FROM pypy:3.6-slim


RUN apt-get update \
    && apt-get install -y gcc libxml2-dev libxslt1-dev python-dev zlib1g-dev \
    && pip install parsedmarc==6.7.4 \
    && rm -rf /root/.cache/ \
    && apt-get purge -y gcc \
    && apt-get autoremove -y \
    && rm -rf /var/lib/{apt,dpkg}/

CMD ["parsedmarc"]
