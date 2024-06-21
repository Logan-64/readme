#  titaniumcore
welcome  to  titaniumcore,  the  open  source  core  of  the  titanium  discord  bot,

##  contributions  welcome!
have  an  improvement  you  want  to  make?  developed  a  new  cog  that  you  want  to  be  in  the  main  bot?  contributions  are  welcome!  make  a  pull  request  and  i'll  take  a  look,  :)

##  included  features
-  wikipedia  and  urban  dictionary  search
-  random  dog  and  cat  images
-  fun  commands  like  the  8  ball  and  fish  command
-  search  spotify  and  get  full  quailty  album  art  (spotify  api  keys  needed)
-  get  lyrics  for  songs
-  get  urls  for  a  song  link  from  any  popular  streaming  service
-  expandable  cog  system  to  allow  you  to  make  your  own  commands

##  credit
**main  code:**  me\
**paged  view  for  playlist,  lyrics,  leaderboard,  etc:**  [rvzwn  on  stack  overflow](https://stackoverflow,com/a/77463524),  modified  by  me

##  self  hosting  titaniumcore
self-hosting  titaniumcore  is  possible,  however  you  must  get  the  required  modules  and  api  tokens  first,

>  [!important]
>  while  i  have  taken  every  precaution  to  block  offensive  content  from  being  displayed  without  a  disclaimer,  it  is  your  responsibility  as  the  bot  host  to  monitor  for  any  offensive  content  posted  using  the  bot,

>  [!caution]
>  when  generating  bot  tokens  and  api  secrets,  do  not  share  them  with  anybody!

###  python  modules
titaniumcore  relies  on  several  python  modules  to  function,  these  modules  can  be  installed  from  pypi  using  pip  or  your  preferred  package  manager,\
\
**installation  command:**\
`pip  install  discord,py  spotipy  wikipedia  colorthief  py-cpuinfo  psutil`

###  discord  bot  token
titaniumcore  requires  a  discord  bot  token  to  function,  the  steps  to  get  one  are  as  follows:
1,  go  to  the  [discord  developer  portal](https://discord,com/developers/applications)  and  log  in  with  your  discord  account,
2,  create  a  new  application  and  fill  in  the  information  required,
3,  go  to  the  `bot`  section,  and  generate  a  new  bot,
4,  give  your  bot  a  username,  and  optionally,  a  pfp  and  banner,
5,  copy  the  bot  token,  and  paste  it  into  the  bot  token  field  in  the  config  file,  due  to  security  reasons,  you  will  only  be  able  to  view  the  bot  token  once  from  discord  developer  portal  before  having  to  generate  a  new  one,

###  spotify  api  key
to  use  the  spotify  commands  in  titaniumcore,  a  spotify  client  id  and  secret  are  required,  if  you  do  not  provide  these,  spotify  commands  will  automatically  be  disabled,  the  steps  to  get  these  are  as  follows:
1,  go  to  the  [spotify  developers  dashboard](https://developer,spotify,com/dashboard),  a  free  or  premium  spotify  account  is  required,
2,  create  a  new  app,  set  the  app  name  and  description  to  whatever  you  please,    no  additional  apis  are  required,
3,  set  the  redirect  uri  to  any  valid  url,  `http://example,com`  is  known  to  work,  then,  create  the  app,
4,  copy  the  client  id  and  secret  for  your  app,  and  paste  them  into  their  respective  fields  in  the  config  file,

###  starting  the  bot
once  you  have  have  installed  the  required  python  modules  and  generated  your  tokens,  you  can  run  the  bot  as  follows:
1,  navigate  to  the  titaniumcore  directory  through  the  terminal,
2,  once  you  are  at  the  titaniumcore  directory,  run  `python  main,py`,  and  monitor  for  any  errors  in  the  terminal,

if  an  error  occurs,  please  create  a  github  issue  and  i  will  take  a  look,

###  generating  a  bot  invite
to  invite  your  instance  of  titaniumcore  to  your  server,  an  invite  is  required,  you  can  use  the  following  template  to  make  a  bot  invite  url:\
`https://discord,com/oauth2/authorize?client_id=(your  client  id)&permissions=964220546112&scope=bot`\
you  will  need  your  discord  client  id  to  make  this  url,  you  can  get  this  from  the  general  information  page  of  your  application  you  generated  earlier  in  discord  developer  portal,

##  included  commands
titaniumcore  comes  with  some  included  commands,  below  is  a  list  of  what  commands  are  in  each  cog  file:
-  **animal  commands**  *(animals,py)*
    -  **animals  cat:**  see  a  random  image  of  a  cat,
    -  **animals  dog:**  see  a  random  image  of  a  dog,
    -  **animals  sand-cat:**  get  a  random  sand  cat  -  requires  /content/sand-cat  to  be  present  and  have  images  inside
-  **bot  utility  commands**  *(bot_utils,py)*
    -  **bot  ping:**  see  the  bot's  latency,
    -  **bot  info:**  view  info  about  the  bot,
    -  **bot  host-info:**  see  information  about  the  bot's  hosting  server,
    -  **bot  send-message:**  send  a  message  through  the  bot  (bot  owner  only),
-  **cog  utility  commands  (bot  owner  only)**  *(cog_utils,py)*
    -  **cogs  load:**  load  a  new  cog,
    -  **cogs  unload:**  unload  a  loaded  cog,
    -  **cogs  reload:**  reload  a  loaded  cog,
    -  **cogs  sync:**  sync  the  command  tree,
-  **leaderboard  commands**  *(leaderboard,py)*
    -  **leaderboard:**  see  the  server  leaderboard,
    -  **lb-control  enable:**  enable  the  server  leaderboard,
    -  **lb-control  enable:**  disable  the  server  leaderboard,
    -  **lb-control  reset:**  reset  the  server  leaderboard,
    -  **lb-control  reset-user:**  reset  a  user  on  the  leaderboard,
-  **misc  commands**  *(misc,py)*
    -  **fun  8ball:**  consult  the  mystical  8  ball  for  an  answer  to  a  question,
    -  **fun  random-num:**  get  a  random  number,
    -  **fun  dice:**  roll  a  dice,
-  **music  commands**  *(music,py)*
    -  **lyrics:**  get  the  lyrics  to  a  song,
-  **bot  utility  commands**  *(server_utils,py)*
    -  **server  icon:**  get  the  current  server's  icon,
    -  **server  info:**  get  info  about  the  current  server,
-  **song  url  command**  *(song-url,py)*
    -  **song-url:**  get  info  about  a  music  streaming  service  url,  powered  by  https://song,link,
-  **spotify  commands**  *(spotify,py)*
    -  **spotify  search:**  search  spotify  for  a  song,  artist  or  album,
    -  **spotify  image:**  get  album  art  for  a  spotify  song,  album  or  playlist  url,
-  **web  search  commands**  *(web_search,py)*
    -  **urban-dictionary:**  search  urban  dictionary,  results  are  mainly  unmoderated  and  may  be  inappropriate,
    -  **wikipedia:**  search  wikipedia  for  an  answer,

##  included  cogs
titaniumcore  also  includes  some  non  command  cogs,  which  are  also  stored  in  the  command  folder,  the  list  is  below:
-  **spotify_autoembed,py**
    -  stores  the  event  handler  for  spotify  auto-embedding,

##  developing  your  own  cogs
titaniumcore  is  modular  and  will  load  compatible  cogs  automatically,

###  cogs  path
the  default  cogs  path  is:\
`(running-path)/commands`,\
this  path  can  be  changed  to  a  path  of  your  selection  in  the  config  file,

###  example  cog
i  have  developed  an  example  cog  that  you  can  look  at  and  modify  to  fit  your  needs,  you  can  find  it  in  `example,py`,  when  you  are  ready  to  use  the  cog,  place  it  in  your  cogs  folder  (`/commands`  by  default),
