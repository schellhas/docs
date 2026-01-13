Managing multiple SSH identities for Git
========================================

.. note::
	Whole site is written by AI (but checked by me)

Step 1: Generate ed25519 SSH keys for each account
--------------------------------------------------

Do this for each account (GitHub, work server, university, personal, etc.). Each key is unique per account.

.. code-block:: bash

	# Work Git server
	ssh-keygen -t ed25519 -C "work@email.com" -f ~/.ssh/id_ed25519_work

	# University Git server
	ssh-keygen -t ed25519 -C "uni@email.com" -f ~/.ssh/id_ed25519_uni

	# Personal GitHub account
	ssh-keygen -t ed25519 -C "personal@email.com" -f ~/.ssh/id_ed25519_personal_github

	# Second GitHub account (if you have one)
	ssh-keygen -t ed25519 -C "personal2@email.com" -f ~/.ssh/id_ed25519_personal2_github

Step 2: Add the keys to SSH-agent
---------------------------------

This ensures SSH can automatically use your keys without entering the passphrase every time.

.. code-block:: bash

	eval "$(ssh-agent -s)"
	ssh-add ~/.ssh/id_ed25519_work
	ssh-add ~/.ssh/id_ed25519_uni
	ssh-add ~/.ssh/id_ed25519_personal_github
	ssh-add ~/.ssh/id_ed25519_personal2_github

Step 3: Add public keys to the corresponding services
------------------------------------------------------

Copy the `.pub` files into the web UI of your Git servers / GitHub accounts.

.. code-block:: bash

	cat ~/.ssh/id_ed25519_work.pub
	cat ~/.ssh/id_ed25519_uni.pub
	cat ~/.ssh/id_ed25519_personal_github.pub
	cat ~/.ssh/id_ed25519_personal2_github.pub

Upload each key to the correct account:

- Work server → work git account
- Uni server → uni git account
- Personal GitHub → personal GitHub account
- Second GitHub → second GitHub account

Step 4: Configure `~/.ssh/config`
---------------------------------

This maps each host alias to its key. You will use these aliases in git clone URLs.

.. code-block:: bash

	# Work server
	Host git_work
		HostName git.work.com
		User git
		IdentityFile ~/.ssh/id_ed25519_work
		IdentitiesOnly yes

	# University server
	Host git_uni
		HostName git.uni.edu
		User git
		IdentityFile ~/.ssh/id_ed25519_uni
		IdentitiesOnly yes

	# Personal GitHub account
	Host personal_github
		HostName github.com
		User git
		IdentityFile ~/.ssh/id_ed25519_personal_github
		IdentitiesOnly yes

	# Second GitHub account
	Host personal2_github
		HostName github.com
		User git
		IdentityFile ~/.ssh/id_ed25519_personal2_github
		IdentitiesOnly yes

Step 5: Test SSH connections
----------------------------

Make sure each key works and connects to the correct account.

.. code-block:: bash

	ssh -T git@git_work
	ssh -T git@git_uni
	ssh -T git@personal_github
	ssh -T git@personal2_github

Expected output:

::

	Hi username! You've successfully authenticated, but GitHub/GitLab does not provide shell access.

Step 6: Clone repositories using the SSH host aliases
------------------------------------------------------

Use the `Host` alias you defined in `~/.ssh/config` instead of the raw domain.

.. code-block:: bash

	# Work repo
	git clone git@git_work:work_username/work_repo.git

	# University repo
	git clone git@git_uni:uni_username/uni_repo.git

	# Personal GitHub repo
	git clone git@personal_github:personal_username/repo.git

	# Second GitHub repo
	git clone git@personal2_github:personal2_username/repo.git

Step 7: Set local user.name and user.email per repo
---------------------------------------------------

This controls commit metadata and is independent of SSH authentication.

.. code-block:: bash

	cd path/to/repo

	# example for work repo
	git config user.name "Work Name"
	git config user.email "work@email.com"

	# example for personal GitHub repo
	git config user.name "Personal Name"
	git config user.email "personal@email.com"

Step 8: Commit and push
-----------------------

.. code-block:: bash

	git add .
	git commit -m "my commit"
	git push

Step 9: Wrong SSH key
---------------------

If Git offers the wrong SSH key (check with `GIT_SSH_COMMAND="ssh -v" git push`), fix it by pointing the remote to the correct SSH host alias.

.. code-block:: bash

	| git remote set-url origin git@host_name:username/repo.git
	| host_name: whatever you called Host in step 4.

Step 10: Notes / best practices
-------------------------------

- Each GitHub account must have its **own unique SSH key**.
- Do **not** reuse keys between accounts.
- Always use **host aliases** from `~/.ssh/config` in your git remotes.
- Local `user.name` and `user.email` only affect commit metadata, not push permission.
- If using GitHub privacy emails, use the noreply email for `user.email` to avoid push errors.
- `ssh-add` only needs to run once per session (or you can add keys to your OS keychain).
- ed25519 keys are recommended over RSA for security and speed.
