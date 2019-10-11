FROM redis

ENV REDIS_PASSWORD test

CMD ["sh", "-c", "exec redis-server --requirepass \"$REDIS_PASSWORD\""]
