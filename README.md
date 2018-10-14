### ActiveSupport
---

https://github.com/rails/rails/tree/master/activesupport

https://railsguides.jp/active_support_core_extensions.html

```
gem install activesupport

gem install rails
rails new myapp
cd myapp
rails server
```

```ruby
# active_support/core_ext/object/blnak.rb
require 'active_support'

def authenticate(controller, &login_procedure)
  token, options = token_and_options(controller.request)
  unless token.blank?
    login_procedure.call(token, options)
  end
end

def set_conditional_cache_control!
  return if self["Cache-Control"].present?
end

host = config[:host].presence || 'Localhost'

"foo".dup
"".dup
1.method(:+).dup
Complex(0).dup

"foo".duplicable?
"".duplicable?
Rational(1).duplicable?
Complex(1).duplicable?
1.method(:+).duplicable?

nil.dup
:my_symbol.dup
1.dup

nil.duplicable?
:my_symbol.duplicable?
1.duplicable?


```

```

```


