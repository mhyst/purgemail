# purgemail
Check gmail account and process or purge undesired email

Based on gmail library from [Charlie Guo - @charlierguo](https://github.com/charlierguo/gmail).

## Why
We spend quite some time manually purging our gmail account removing unwanted junk that we are too lazy to unsuscribe from. Other times we want to label some emails, or we don't want to read them at the momment. We find annoying to opening or marking them as readed. I sometimes star some mails to read them later and I find myself doing that repetitive work day after day. I know all can be done easily using Gmail own filters, but for some matter, you may need extra help. This is for that. Well, I find easier to write some rules on a text file and launching this script before opening gmail.

## How
By default, this script processes unread mails. It attempts to login into your gmail account and then, after loading and parsing the rules file, processes every mail and tests if some rule matches with the source (from) of the mail. If the mail matches one rule, several actions can be applied to the same email.

## Rules format
Search string#action[=data][:action[=data]*]

Rules file example:
```
Spain Report#label=News:read
dzoom#label=Bulletin:read
Twitter#delete
schneier@schneier.com#label=BruceSchneier:read
Hofmann#delete
EFF#star:label=EFF:read
@fsf.org#star:label=FSF:read
Enrique Dans#star:label=EDans:read
Medium Daily Digest#delete
Google+#delete
```

After one search string, you can specify several rules separated by ":". If one action requires some extra data, you can write it like "action=data". Actions will be exececuted in the order you've writen them. Available actions are: read, star, label, delete, move and archive.

## Work in progress
I just started writting the script. Surely as time passes I will find some ways to improve it. I accept suggestions and criticism.

## Contact
Julio Serrano "mhyst"
[mhysterio at gmail dot com](mailto:mhysterio@gmail.com)
