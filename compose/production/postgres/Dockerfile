FROM postgres:17

COPY ./compose/production/postgres/maintenance /usr/local/bin/maintenance
RUN chmod +x /usr/local/bin/maintenance/* || true
RUN if [ -d /usr/local/bin/maintenance ]; then \
    mv /usr/local/bin/maintenance/* /usr/local/bin/ 2>/dev/null || true; \
    rmdir /usr/local/bin/maintenance 2>/dev/null || true; \
    fi
