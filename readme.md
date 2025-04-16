# Only for Linux, WSL (Debian Based Distros)

Step 1
-------------------------------------------------------------------------------------------------------------
```
sudo apt update
```

```
sudo apt install python-is-python3 virtualenv apt-transport-https ca-certificates gnupg curl python3.12-venv
```

Step 2
-------------------------------------------------------------------------------------------------------------
**For newer distributions (Debian 9+ or Ubuntu 18.04+) -

```
curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo gpg --dearmor -o /usr/share/keyrings/cloud.google.gpg
```

```
echo "deb [signed-by=/usr/share/keyrings/cloud.google.gpg] https://packages.cloud.google.com/apt cloud-sdk main" | sudo tee -a /etc/apt/sources.list.d/google-cloud-sdk.list
```

**For older distributions - 

```
curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key --keyring /usr/share/keyrings/cloud.google.gpg add -
```

```
echo "deb https://packages.cloud.google.com/apt cloud-sdk main" | sudo tee -a /etc/apt/sources.list.d/google-cloud-sdk.list
```

Step 3
-------------------------------------------------------------------------------------------------------------
```
sudo apt-get update && sudo apt-get install google-cloud-cli
```

```
gcloud init #optional
```

you don't have to sign in to the account

```
sudo apt-get install google-cloud-cli-app-engine-python google-cloud-cli-datastore-emulator
```
Step 4
---------------------------------------------------------------------
1. Search for google-cloud-sdk folder. it should be in the /lib or ~/ directory or search for the folder in the files app. 
2. After locating the folder, go to /bin directory and copy the absolute path
3. clone the repository 
4. open terminal or cmd in the repository folder. and run --absolute-path-copied-before--/dev_appserver.py app.yaml
5. visit http://localhost:8080


---------------------------------------------------------------------
Refer https://cloud.google.com/sdk/docs/install for more information on gcloud cli installation