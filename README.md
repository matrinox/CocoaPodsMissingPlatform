# CocoaPodsMissingPlatform
CocoaPods example that produces this warning: https://github.com/CocoaPods/CocoaPods/issues/3797

You should see this error:
-----

```bash
(master) [0<-17/17(5)] CocoaPodsMissingPlatform: pod install
~/.rvm/gems/ruby-2.2.2@global/gems/cocoapods-0.38.0/lib/cocoapods/command.rb:130: warning: Insecure world writable dir /usr/local/bin in PATH, mode 040777
Updating local specs repositories

CocoaPods 0.38.1 is available.
To update use: `gem install cocoapods`
Until we reach version 1.0 the features of CocoaPods can and will change.
We strongly recommend that you use the latest version at all times.

For more information see http://blog.cocoapods.org
and the CHANGELOG for this version http://git.io/BaH8pQ.

Analyzing dependencies
Downloading dependencies
Generating Pods project
Integrating client project
Sending stats

――― MARKDOWN TEMPLATE ―――――――――――――――――――――――――――――――――――――――――――――――――――――――――――

### Command

```
~/.rvm/gems/ruby-2.2.2/bin/pod install
```

### Report

* What did you do?

* What did you expect to happen?

* What happened instead?


### Stack

```
CocoaPods : 0.38.0
Ruby : ruby 2.2.2p95 (2015-04-13 revision 50295) [x86_64-darwin14]
RubyGems : 2.4.6
Host : Mac OS X 10.11 (15A216g)
Xcode : 6.4 (6E35b)
Git : git version 2.3.2 (Apple Git-55)
Ruby lib dir : ~/.rvm/rubies/ruby-2.2.2/lib
Repositories : master - https://github.com/CocoaPods/Specs.git @ 4683b5599b9fcb6dacf56ed08537f4ce668d397d
```

### Plugins

```
cocoapods-plugins : 0.4.2
cocoapods-stats   : 0.5.3
cocoapods-trunk   : 0.6.1
cocoapods-try     : 0.4.5
```

### Podfile

```ruby
platform :osx, "10.10"
```

### Error

```
NoMethodError - undefined method `include?' for nil:NilClass
~/.rvm/gems/ruby-2.2.2@global/gems/xcodeproj-0.26.2/lib/xcodeproj/project/object/native_target.rb:92:in `platform_name'
~/.rvm/gems/ruby-2.2.2@global/gems/cocoapods-stats-0.5.3/lib/cocoapods_stats/target_mapper.rb:36:in `block (2 levels) in pods_from_project'
~/.rvm/gems/ruby-2.2.2@global/gems/cocoapods-stats-0.5.3/lib/cocoapods_stats/target_mapper.rb:27:in `map'
~/.rvm/gems/ruby-2.2.2@global/gems/cocoapods-stats-0.5.3/lib/cocoapods_stats/target_mapper.rb:27:in `block in pods_from_project'
~/.rvm/gems/ruby-2.2.2@global/gems/cocoapods-stats-0.5.3/lib/cocoapods_stats/target_mapper.rb:9:in `each'
~/.rvm/gems/ruby-2.2.2@global/gems/cocoapods-stats-0.5.3/lib/cocoapods_stats/target_mapper.rb:9:in `flat_map'
~/.rvm/gems/ruby-2.2.2@global/gems/cocoapods-stats-0.5.3/lib/cocoapods_stats/target_mapper.rb:9:in `pods_from_project'
~/.rvm/gems/ruby-2.2.2@global/gems/cocoapods-stats-0.5.3/lib/cocoapods_plugin.rb:31:in `block (2 levels) in <module:CocoaPodsStats>'
~/.rvm/gems/ruby-2.2.2@global/gems/cocoapods-0.38.0/lib/cocoapods/user_interface.rb:80:in `titled_section'
~/.rvm/gems/ruby-2.2.2@global/gems/cocoapods-stats-0.5.3/lib/cocoapods_plugin.rb:27:in `block in <module:CocoaPodsStats>'
~/.rvm/gems/ruby-2.2.2@global/gems/cocoapods-0.38.0/lib/cocoapods/hooks_manager.rb:115:in `call'
~/.rvm/gems/ruby-2.2.2@global/gems/cocoapods-0.38.0/lib/cocoapods/hooks_manager.rb:115:in `block (3 levels) in run'
~/.rvm/gems/ruby-2.2.2@global/gems/cocoapods-0.38.0/lib/cocoapods/user_interface.rb:140:in `message'
~/.rvm/gems/ruby-2.2.2@global/gems/cocoapods-0.38.0/lib/cocoapods/hooks_manager.rb:111:in `block (2 levels) in run'
~/.rvm/gems/ruby-2.2.2@global/gems/cocoapods-0.38.0/lib/cocoapods/hooks_manager.rb:109:in `each'
~/.rvm/gems/ruby-2.2.2@global/gems/cocoapods-0.38.0/lib/cocoapods/hooks_manager.rb:109:in `block in run'
~/.rvm/gems/ruby-2.2.2@global/gems/cocoapods-0.38.0/lib/cocoapods/user_interface.rb:140:in `message'
~/.rvm/gems/ruby-2.2.2@global/gems/cocoapods-0.38.0/lib/cocoapods/hooks_manager.rb:108:in `run'
~/.rvm/gems/ruby-2.2.2@global/gems/cocoapods-0.38.0/lib/cocoapods/installer.rb:448:in `run_plugins_post_install_hooks'
~/.rvm/gems/ruby-2.2.2@global/gems/cocoapods-0.38.0/lib/cocoapods/installer.rb:440:in `perform_post_install_actions'
~/.rvm/gems/ruby-2.2.2@global/gems/cocoapods-0.38.0/lib/cocoapods/installer.rb:111:in `install!'
~/.rvm/gems/ruby-2.2.2@global/gems/cocoapods-0.38.0/lib/cocoapods/command/project.rb:71:in `run_install_with_update'
~/.rvm/gems/ruby-2.2.2@global/gems/cocoapods-0.38.0/lib/cocoapods/command/project.rb:101:in `run'
~/.rvm/gems/ruby-2.2.2@global/gems/claide-0.9.1/lib/claide/command.rb:312:in `run'
~/.rvm/gems/ruby-2.2.2@global/gems/cocoapods-0.38.0/lib/cocoapods/command.rb:48:in `run'
~/.rvm/gems/ruby-2.2.2@global/gems/cocoapods-0.38.0/bin/pod:44:in `<top (required)>'
~/.rvm/gems/ruby-2.2.2/bin/pod:23:in `load'
~/.rvm/gems/ruby-2.2.2/bin/pod:23:in `<main>'
~/.rvm/gems/ruby-2.2.2/bin/ruby_executable_hooks:15:in `eval'
~/.rvm/gems/ruby-2.2.2/bin/ruby_executable_hooks:15:in `<main>'
```
