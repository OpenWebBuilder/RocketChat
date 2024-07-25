sch: https://www.google.com/search?q=rocketchat+loads+forever

# Solution:
https://forums.rocket.chat/t/rocket-chat-docker-server-running-but-page-stuck-on-the-three-dots-loading-page/17979

>I found the cause of the issue (or atleast mine). Apparently even when you run docker compose down, it does not totally wipe the mongodb data. I originally had run the docker compose without changing the ROOT_URL.
>
>After hours and hours of searching, I finally stumbled upon the answer. Run the command “docker compose down --volumes” while the containers are running and this will wipe the mongodb.
>
>Make sure your .env file is correct and run “docker compose up -d” again and it should change the site URL to what you have listed in the .env file.
>
>Hope this helps!
