FROM debian:12-slim
RUN apt-get update -qq && apt-get install -y curl wait-for-it iputils-ping iproute2 \
    && useradd -r -u 1001 -s /bin/false appuser
COPY entrypoint.sh /usr/local/bin/entrypoint
RUN chmod +x /usr/local/bin/entrypoint
USER appuser
ENTRYPOINT [ "/usr/local/bin/entrypoint" ]