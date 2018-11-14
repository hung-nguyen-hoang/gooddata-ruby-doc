---
id: computing_existing_report
author: GoodData
sidebar_label: Computing Report
title: Computing Report
---

Problem
-------

You have an existing report and you would like to execute it
programmatically.

Solution
--------


```ruby
# encoding: utf-8

require 'gooddata'

GoodData.with_connection do |c|
  GoodData.with_project('project_id') do |project|
    puts project.reports(1234).execute
  end
end
```