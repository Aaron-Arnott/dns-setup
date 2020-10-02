FROM pihole/pihole:latest

COPY ./adlists.list /etc/pihole/adlists.list
RUN for word in $(cat "/etc/pihole/adlists.list"); do \
      sqlite3 /etc/pihole/gravity.db "INSERT INTO adlist(address, enabled, date_added, date_modified, comment) VALUES('${word}', 1, strftime('%s', 'now'), strftime('%s', 'now'), '');" ;\
    done
