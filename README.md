# discourse-user-creator

Create an activated user, optionally assigning to group

### Usage:

    ./create-user 'Real Name' email user_name group_id password

The following environment variables need to be set

    DISCOURSE_URL=https://yourdiscoursesite.com
    DISCOURSE_API_KEY="get from yourdiscoursesite.com/admin/api/keys"
    DISCOURSE_API_USER=system
    DISCOURSE_PASSWORD="Thisisstrangelysafepassword"

The script will read these values from `CREATE_USER_DEFAULTS`, probably deleting them if you set them elsewhere, arguably a bug.

Get your API key from https://yoursite/admin/api/keys

To find the group ID, see https://yourdiscoursesite.com/admin/groups.json. A tool like Chrome's [JSONView](https://chrome.google.com/webstore/detail/jsonview/chklaanhfefbnpoihckbnefhakgolnmc?utm_source=chrome-app-launcher-info-dialog) or similarly-named [JSONView](https://addons.mozilla.org/en-US/firefox/addon/jsonview/) for Chrome will make it easier to read JSON files in your browser.

TODO: Should check to see whether the user actually got created.
