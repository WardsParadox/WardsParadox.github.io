---
layout: post
title: "Adding a \"Coming Soon\" Ribbon to the Munki Showcase"
date: "2015-12-12"
---

I have been doing some testing and it seems that with the latest OS X El Capitan release, our district can finally move to El Capitan. At the same time I have been doing some testing of Office 2016 for Mac. I have been moving our district to deploying software with Munki. It's been two years and has already saved us hundreds of man hours.

I was aware of the conditional items ability with Munki. I wanted a little bit of time in case and final issues came about. So I set the optional installs to become available to be the 2nd of January, 2016; the day before our teachers and staff members came back. Make sure you escape the greater than symbol
{% highlight xml %}
<key>conditional_items</key>
<array>
  <dict>
    <key>condition</key>
    <string>date `&gt;` CAST("2016-01-02T00:00:00Z", "NSDate")</string>
    <key>optional_installs</key>
    <array>
      <string>InstallOSX</string>
      <string>MSOffice2016</string>
    </array>
  </dict>
</array>
{% endhighlight %}
