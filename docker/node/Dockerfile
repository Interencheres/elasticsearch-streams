FROM 776403767600.dkr.ecr.eu-west-1.amazonaws.com/cpm-docker-base-node:22.4.1_2

# Switch to root for setup
USER root

RUN mkdir -p /srv/cpm-elasticsearch-streams/

# Switch back to app user
USER app

WORKDIR /srv/cpm-elasticsearch-streams/
HEALTHCHECK --interval=5s --timeout=20s --retries=1 CMD test -f .ready

CMD [ "bash", "-c", "npm ci && touch .ready && sleep infinity" ]
