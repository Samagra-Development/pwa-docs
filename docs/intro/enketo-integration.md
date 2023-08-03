---
title: Enketo Integration ☁️
sidebar_label: Enketo Integration ☁️
slug: /enketo-integration
hide_table_of_contents: true
# demoUrl: https://passbook.familyid.samagra.io/
demoSourceUrl: https://github.com/Samagra-Development/pwa-docs
---

<head>
  <title>Enketo Integration ☁️</title>
  <meta name="description" />
</head>

Enketo Forms is an <b>open-source</b> software tool that simplifies the creation and deployment of mobile-friendly web forms for data collection. With its user-friendly interface, offline functionality, and support for advanced features like data validation and skip logic, Enketo Forms provides a flexible and accessible solution for designing and managing forms on various devices. It is a popular choice among researchers, surveyors, and organizations looking for a lightweight and adaptable tool to streamline their data collection process.

## How does it integrate with PWA?
Any app is incomplete without having some form of Data Collection. This is where Enketo Forms come into play in this PWA. We are using Enketo Forms for the purpose of data collection at an immensely large scale with hundreds of different forms which would be an extremely hard task if every form was made in React itself thus bringing in Enketo in the picture.

### Some of the key features

1. It can render a pretty complex form with multiple levels, options, inputs, etc

    <video height='500' controls autoplay >
      <source src="/assets/enketo-1.mp4" type="video/mp4" />
    </video>

2. Works completely offline, everything from filling the form, uploading images, submitting the form works offline.

    <video height='500' controls autoplay >
      <source src="/assets/enketo-3.mp4" type="video/mp4" />
    </video>

3. Supports submission queue for multiple submission. If you have multiple submissions for a particular form, all the submissions can be queued and submitted to the server one by one easily.

    <video height='500' controls autoplay >
      <source src="/assets/enketo-4.mp4" type="video/mp4" />
    </video>

4. Upload files to custom storage service easily, you can configure to use any of your own hosted storaged servcies like AWS S3, Glacier, etc

    <video height='500' controls autoplay >
      <source src="/assets/enketo-5.mp4" type="video/mp4" />
    </video>