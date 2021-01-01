# Jump to Flask - Pybo Project

## How to setup

1. Create a virtual environment using virtualenv

   ```shell
   $ virtualenv venv
   ```

2. Activate the virtual environment

   ```shell
   $ .\venv\Scripts\activate
   $(venv)
   ```

3. Run setup_env.cmd (Command Prompt) or setup_env.ps1 (Powershell) if on Windows to set up environment variables

   ```shell
   $(venv) .\setup_env.cmd # Command prompt
   ```

   ```shell
   $(venv) .\setup_env.ps1 # Powershell
   ```

4. Initialize database

   - You only have to do this once!

   ```shell
   $(venv) flask db init # This will create `migrations` folder
   ```

## Run the server

1. Activate the virtual environment

   ```shell
   $ .\venv\Scripts\activate
   $(venv)
   ```

2. Run setup_env.cmd (Command Prompt) or setup_env.ps1 (Powershell) if on Windows to set up environment variables

   ```shell
   $(venv) .\setup_env.cmd # Command prompt
   ```

   ```shell
   $(venv) .\setup_env.ps1 # Powershell
   ```

3. Run the server

   ```shell
   flask run
   ```

## Handling changes in the database

1. If there are new models or modifications to existing models in the DB

   ```shell
   $(env) flask db migrate # Creates a revision file in migrations/versions/
   ```

2. To apply the modifications to the DB

   ```shell
   $(env) flask db upgrade # Upgrade DB using the revision file
   ```
