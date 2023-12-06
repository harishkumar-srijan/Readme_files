### DDev Environment Set Up

> [!IMPORTANT]
> colima and ddev install globally

#### colima and ddev setup local:

```
- `colima start; ddev start;` — (Run cammand in new project)
- `ddev config` (One time for in new project - ddev port setup like)
- `ddev composer require drush/drush` - (drush setup in new project )
- `ddev start`
- `ddev composer i` or (COMPOSER_MEMORY_LIMIT=-1 composer i) (if composer have memoery issue)
- `drush cr`
- `ddev db-import web/1Decwebformpoc.sql` or `ddev import-db --src=./web/data4.sql` (db name)
- `ddev describe` (for check database url and details) —> http://localhost:49885/index.php
```

> [!TIP]
> useful commands

```
- ddev ssh;
- ddev describe;
- ddev help;
- ddev restart;
- ddev start;
- ddev stop;
- colima start;
- colima stop;
- colima delete;
```

### Docker and Lando

#### Project Set:

```
- git clone qbmonkfkl7ptg@git.uk-1.platform.sh:qbmonkfkl7ptg.git webformpoc
- Provide publice key if need (create your self — https://devqa.io/install-git-mac-generate-ssh-keys/ )
- after create copy file in my profile —> SSH keys
- if need API tokens —> my profile —> API tokens —> create (meanwhile installing the project)
```

#### Lando:

```
- `lando init` (one time for new project - intial the lando set up)
- `lando start`
- `lando ssh —> composer i` (COMPOSER_MEMORY_LIMIT=-1 composer i) —> after we can run here (here we run drush cr, drush cim )
- `drush cr`
- `lando db-import web/1Decwebformpoc.sql` (db name) run this command not need to set up the project
- `lando info` (for check database url and details) —> http://localhost:49885/index.php
```

**Restart system and again**

```
- lando start
- lando destroy
- lando rebuild
```

> [!IMPORTANT]
> if Docker not work in any condition

**if Docker not work in any condition**

```
- docker stop $(docker ps -a -q)
- docker rm $(docker ps -a -q)
- docker volume rm $(docker volume ls -q)
```

> [!CAUTION]
> FATA[0000] error starting vm: error at 'starting': exit status 1

```
- colima delete
- colima start
```

> [!NOTE]
> its remove the database intstall the database again
