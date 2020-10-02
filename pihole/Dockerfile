FROM pihole/pihole:latest

COPY ./adlists.sql /etc/pihole/adlists.sql
RUN sqlite3 /etc/pihole/gravity.db ".read /etc/pihole/adlists.sql"
