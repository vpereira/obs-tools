# Leap 15.1
FROM registry.opensuse.org/home/vpereirabr/dockerimages/containers/obs-tools/base:latest

COPY .  /home/frontend/obs-package-status

RUN chown -R frontend:users /home/frontend/

WORKDIR /home/frontend/obs-package-status

RUN bundler.ruby2.5 install

USER frontend

ENTRYPOINT ["./entrypoint.sh"]

CMD ["./status-check.rb"]
