FROM 1password/scim:v2.8.5

ENV OP_REDIS_SSL_ENABLED=1

CMD /op-scim/op-scim \
		--port="${PORT}" \
		--redis-enable-ssl="1" \
		--redis-url="${OP_REDIS_TLS_URL}" \
		--session="${OP_SESSION}"
