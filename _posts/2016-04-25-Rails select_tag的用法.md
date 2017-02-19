---
layout: post
title:  "Rails select_tag的用法"
date:   2016-04-25 11:46:01 +0800
---
select_tag(name, option_tags = nil, options = {}) public

Creates a dropdown selection box, or if the :multiple option is set to true, a multiple choice selection box.

Helpers::FormOptions can be used to create common select boxes such as countries, time zones, or associated records. option_tags is a string containing the option tags for the select box.

Options

:multiple - If set to true the selection will allow multiple choices.

:disabled - If set to true, the user will not be able to use this input.

:include_blank - If set to true, an empty option will be created. If set to a string, the string will be used as the option’s content and the value will be empty.

:prompt - Create a prompt option with blank value and the text asking user to select something.

Any other key creates standard HTML attributes for the tag.