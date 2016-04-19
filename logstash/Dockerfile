FROM logstash:latest

# Make .m2 accessible to logstash user, otherwise logstash won't start
RUN mkdir -p /var/lib/logstash/.m2
RUN ln -s /var/lib/logstash/.m2 /root/.m2
RUN curl -L https://rubygems.org/downloads/logstash-codec-protobuf-0.1.1.gem > /tmp/logstash-codec-protobuf.gem
RUN /opt/logstash/bin/logstash-plugin install /tmp/logstash-codec-protobuf.gem

ENV PATH /opt/logstash/vendor/jruby/bin/:$PATH

