# Update NodeJS app

To update all dependencies in a NodeJS app:

1.  Install `npm-check-updates` globally:

    ```bash
    npm install -g npm-check-updates
    ```

2.  Run the script

    ```bash
    ncu -u
    ```

3.  Install the new dependencies

    ```bash
    npm install
    ```

## For Vite apps

If the app is a Vite app, run `ncu '/vite|@vitejs' -u` instead of `ncu -u`.
