
#### Crontab Commands

The crontab command is used to edit, list, and remove the cron jobs:

-   **crontab -e** To edit current user’s crontab file
-   **crontab -l** To display contents of the crontab file
-   **crontab -u [username]** To edit any other user’s crontab file
-   **crontab -r** To remove the crontab file of the current user’s
-   **crontab -i** To display a prompt before removing the current user’s crontab file

---


#### Service cron
##### Start cron

```shell
sudo service cron start
```

##### Restart cron

```shell
sudo service cron restart
```

##### Stop cron

```shell
sudo service cron stop
```

##### Status cron

```shell
sudo service cron status
```

### Examples of Cron Jobs

Here are a few examples of cron jobs:

**Run a cron job every 15 minutes**

To schedule a cron job to run every 15 minutes, add the below line in the crontab file:


```console
*/15 * * * * command/script
```


**Run a cron job at 5 am every day**

To schedule a cron job to run at 5 am every day, add the below line in the crontab file:


```shell
0 5 * * * command/script
```


