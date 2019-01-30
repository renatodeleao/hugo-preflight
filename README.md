# hugo-preflight
Messing around with "world’s fastest framework for building websites"

## Things to remember
- In a section (folder), when an `_index.md` will turn into a list page default. `index.md` (no underscore) will turn into a default single.
- Cache and livereload sometimes is weird. If your suspecting some weird behaviour, for sanity check restart the server and empty your browser cache.
- That "lazy blogger menu" becomes weird with all the subsections customizations. maybe i'm doing something wrong, but i renders supper weird. It's better to do it by hand for now.
- if you and "index" functionalities to subsections `content/section/subsection/_index.md`. Those section pages are excluded from `{{ range .Pages}}` scope on the parent section. I believe this is intened, Buut you always have `.Site

## Mind-blowing discoveries
- Sub-section layout overrides via `type` + `layout`, that points to a `layouts/<type>/<layout>.html`. This is freaking amazing.
  - To make things a breeze, you can create an archetype for nested content by using `hugo new --kind subsectionArchertype section/subsection/mycontent.md`. This ensures that you consistently create content with the correct layouts.
- Update: I discover that creating `layouts/<section>/<section>.html` or `layouts/section/<section>/{list,single}.html`also points to the a custom layout without frontmatter


## General thoughs
- community supporters are way to "defensive" when replying on thread where subject is "dumb question" when in fact there's no such thing. That can create a harsh environment for beginners _a la stackoverflow_ where you have afraid of asking questions.
- Documentation is fairly complete and extensive for a <1.0 version so congrats. One thing to notice is that no written with a "beginner's mind". That's is really hard to do, I know, an when your documenting something the hardest thing is to look at it with fresh unbiased mind. Wihout those videos, most beginnesr wouldn't even know how to start without hacking their way through a theme and trying to find the relashionships from layout with content by trial and error (that's what i did). If you want to use hugo, and you're not the most poficient developer be prepared for at least ~40 hours to get confortable with it.

