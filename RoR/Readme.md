## 1. jquery-gem이용 시, jquery가 define되지 않는 경우

```ruby
# assets/views/layouts/application.html.erb
<%= javascript_pack_tag "application" %>
를
<%= javascript_include_tag "application" %>
로 수정
```

## 2. Rails: Sprockets::Rails::Helper::AssetNotPrecompiled in development 에러

```ruby
# config/environments.development.rb

config.assets.check_precompiled_asset = false

추가
```

