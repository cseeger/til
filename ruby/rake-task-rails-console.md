# Running a rake task in `rails console`

Pretty neat trick to run a rake task when you only have access to `rails console`.

```ruby
require 'rake'
<APP_NAME>::Application.load_tasks
Rake::Task['my_task'].invoke
```
