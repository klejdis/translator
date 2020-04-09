Project Assesment:

Generally the code looks ok, it is formated,controllers method names are camelCase,repository patern is implemented
which makes controller more clean.

But one the other side i see that:
 - Form Requests are not being used to validate requests, this makes Repository cluttered
 - The Roles and Permission are not dynamic, but hardcodded on env
 - getting logged in user from request is redundant, its easier with global helper function auth()->user()
   olso adds extra dependency on Repository Methods
 - Translations are hardcodded on responses, no language files used
 - Http status codes are not used. its more RESTApi friendly
 - When creating, editing database transaction and try catch must be used to prevent unexpected bevaviour
 - Rote Model Binding is not Used
 - Parameters on methods are not specified what type they are, this may lead to unexpected bevaviour or
   doing extra check which makes code clutterd
 - Comments are not used to explain code blocks, it is hard to understand if new to project

On the logic level it is hard to tell because i cannot fully understand what the aplication logic is
but judging from how it looks it needs refactor :)


