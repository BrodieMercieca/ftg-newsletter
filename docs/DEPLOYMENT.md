# Deployment

This HOW-TO describes the publishing process from receiving the content
to making its way in front of the entire school.

## Repository

All code is stored in version control located at 
https://bitbucket.org/mfellows/onegeek-ftg-newsletter/admin/deploy-keys/. This
allows us to back-up previous versions and perform simple deployments.

## Pre-requisites

1. All code checked in and pushed to BitBucket
1. All code reviewed and working on local development machine
1. Latest release has been given a git tag with `git tag -a "20161017" -m "October 2016 edition!"`
1. ...

##
### Step 1: SSH onto the Pi

```
ssh bmercieca@underthegumtree.com.au
# <enter password>
```

### Step 2: Change to the deployment user

```
sudo su - deployment
```

### Step 3: Pull the latest code

```
cd /opt/underthegumtree/onegeek-ftg-newsletter/
git pull
```

### Step 4: Check the site is working!

Head to http://underthegumtree.com.au and make sure everything looks OK!

### Step n: Profit!

:)

## Rolling back a deployment

OK, don't panic - we can fix this!!

We just need to go back to the last working tag, let's find all available ones:

```
cd /opt/underthegumtree/onegeek-ftg-newsletter/
git tag 
```

Find the last tag, remembering that each tag should be by date, and then run:

`git co <TAG>`

Now go and work out what happened (you might want to talk to Matt ;) )
