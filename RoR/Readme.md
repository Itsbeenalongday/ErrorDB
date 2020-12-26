## 1. jquery-gem이용 시, jquery가 define되지 않는 경우

```ruby
# assets/views/layouts/application.html.erb
<%= javascript_pack_tag "application" %>
를
<%= javascript_include_tag "application" %>
로 수정
```


