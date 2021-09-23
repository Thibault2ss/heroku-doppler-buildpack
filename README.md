# Heroku Doppler Buildpack

This buildpack injects Doppler env variables in your app. Doppler variables are injected before any of your processes defined in your Procfile, thanks to a [.profile.d script](https://devcenter.heroku.com/articles/buildpack-api#profile-d-scripts).

## Setup

Add this buildpack to your heroku app, and add heroku env variables in your app:

2 options:

1. Doppler Service Token only (access to one config)
   - `DOPPLER_TOKEN`
2. Doppler personal Token + project + config
   - `DOPPLER_TOKEN`
   - `DOPPLER_PROJECT`
   - `DOPPLER_CONFIG`

That's it, your app now has access to doppler envs (eg `process.ENV.YOUR_VAR` in node) 🎉
