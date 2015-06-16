# Jenkins Rackspace Canon(tm) Theme

CSS and JS to implement [Rackspace Canon](http://canon.rackspace.com/) as
a theme for [Jenkins CI](http://jenkins-ci.org/).

This fork removes the Rackspace logo to use the Jenkins one by default.

Compatible with Jenkins UI post-1.572.

Last tested with 1.609.1.

### Before

![Before](CanonJenkinsBefore.png "Before")

### After

![After](CanonJenkinsAfter.png "After")

## CDN URLs

### HTTPS

CSS: https://raw.githubusercontent.com/zyegfryed/canon-jenkins/master/style.css

JS: https://raw.githubusercontent.com/zyegfryed/canon-jenkins/master/app.js

**Note:** these URLs are for the Jenkins UI redesign as of 1.572.

## Usage

1. Install the [Simple Theme Plugin for
   Jenkins](https://wiki.jenkins-ci.org/display/JENKINS/Simple+Theme+Plugin)
2. Navigate to Jenkins > Manage Jenkins > Configure System > Theme
3. Set _URL of theme CSS_ to
   `https://raw.githubusercontent.com/zyegfryed/canon-jenkins/master/style.css`
   (or another URL of your setting/choosing)
4. Set _URL of theme JS_ to
   `https://raw.githubusercontent.com/zyegfryed/canon-jenkins/master/app.js`
   (or another URL of your setting/choosing)

## Building

```
npm install
npm install -g grunt-cli
grunt
```

## To manually change SimpleTheme CSS and JS values

1. Edit: `$JENKINS_HOME/org.codefirst.SimpleThemeDecorator.xml` with code below
2. Restart Jenkins

```
<?xml version='1.0' encoding='UTF-8'?>
<org.codefirst.SimpleThemeDecorator plugin="simple-theme-plugin@0.3">
  <cssUrl>https://raw.githubusercontent.com/zyegfryed/canon-jenkins/master/style.css</cssUrl>
  <jsUrl>https://raw.githubusercontent.com/zyegfryed/canon-jenkins/master/app.js</jsUrl>
</org.codefirst.SimpleThemeDecorator>
```
