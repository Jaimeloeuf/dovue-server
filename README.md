# Mono-repo for DoVue backend server apps
This repo contains all the backend server apps for the [DoVue](https://github.com/Jaimeloeuf/DoVue) project.  
The DoVue project is currently powered by a suite of firebase tools but will be slowly transitioning away from firebase.

## Services in this mono-repo
- IAM
- Backup
- Realtime syncing
- Payment

## Features provided to the user
Below are a list of features that should be built out for the user.  
Those with the (MVP) indicator at the end, tags it as a feature to be build as part of the Minimum Viable Product

- Identity and data security (MVP)
    - Secure log in and out
    - Secure data, meaning notes only avail to authenticated users.
- Mail service (MVP)
    - Used to notify users of things like Account and security related things
- Automatic Backup service
    - Used for automatically backing the users' notes while the user adds more in real time
    - Automatic data pull from the secure backup upon signing in on a new device.
- Payment service
    - For purchase of premium features.
- 

## Notes definition
Each note is encapsulated in a Note Object, which can and will be used in JSON form.  
Each JSON will hold one note, and they can be put in an array to transmit data for multiple notes at once
The JSON structure should look like what's shown below:
{
    timestamp: [
        created,
        last_edit,
        archived_at,
        trashed_at
    ]
}