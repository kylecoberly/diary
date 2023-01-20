# Diary

A (currently) very simple diary for Nextcloud

## Building Locally

1. Install PHP as well as the `xml` and `mbstring` extensions with `sudo apt install php php-xml php-mbstring`
2. Install Node via [nvm](https://github.com/nvm-sh/nvm)
3. Install dependencies and run app build with `make`
4. Mount this repo in the Nextcloud docker image with `docker run --rm -p 8080:80 -v ~/path/to/diary:/var/www/html/apps/diary ghcr.io/juliushaertl/nextcloud-dev-php80:latest`. Make sure to update the first path to the root of this repo.
5. In another terminal process, enable continuous builds by running `npm run watch`
6. Navigate to the app in your browser at `localhost:8080`
7. Login with `admin` / `admin`
8. Go to "Apps" in main menu
9. Scroll to "Diary" authorize enabling the untested app. The page will reload. Scroll down to "Diary" again and enable it.

The Diary app will now be available in Nextcloud and will reflect the state of the local repo.
