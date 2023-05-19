### Local environment setup

Install the ddev on you system.
Clone the repo. Go that repo cloned via terminal.
Run ddev to start.

```bash
ddev start
```

Once DDEV has been setup successfully, it will display the links in the terminal. Next run the following to fetch all dependencies.

```bash
ddev composer install
```

[Download the database copy](https://drive.google.com/file/d/1WRVMSSerDPAvzHyCc6UU-j8tCv2Chq9L/view?usp=sharing) and move it to your directory. Use this command to import it. Make sure the file name matches.

```bash
ddev import-db --src=db-export.sql
```

Once the database is imported, you may want to rebuild the cache and then run the configuration import and database update commands.

```bash
ddev drush cr
ddev drush cim
ddev drush updb
```
