# Convert any EBUP book to audio book.

## Reqiored
Environment GOOGLE_APPLICATION_CREDENTIALS variable pointing to  service_account.json

## Build
docker build -t convertaudio .

## Run
docker run  --rm -it -v $HOME/Desktop:/media  convertaudio test.epub

Have fun!
