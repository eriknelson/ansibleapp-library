FROM ansibleapp/ansibleapp-base
# MAINTAINER {{ $MAINTAINER }}

LABEL "com.redhat.apb.version"="0.1.0"
LABEL "com.redhat.apb.spec"=\
"aWQ6IDg0ZTgxNzNlLTVjZWQtNDQ4OS05YjRkLWFhYzdlNzc5YzQ3ZQpuYW1lOiBjdXJsY3JlZHMt\
YXBiCmltYWdlOiBlcmlrbmVsc29uL2N1cmxjcmVkcy1hcGIKZGVzY3JpcHRpb246IGN1cmwgbW9j\
ayBjcmVkZW50aWFscyBmcm9tIGEgdXJsIGFuZCByZXR1cm4gdGhlbQpiaW5kYWJsZTogdHJ1ZQph\
c3luYzogb3B0aW9uYWwKcGFyYW1ldGVyczoKICAtIG5hbWU6IHVybAogICAgZGVzY3JpcHRpb246\
IHVybCB0byBwdWxsIG1vY2sgY3JlZGVudGlhbHMgZnJvbQogICAgdHlwZTogc3RyaW5nCg=="
ADD ansible /opt/ansible
ADD ansibleapp /opt/ansibleapp

RUN useradd -u 1001 -r -g 0 -M -b /opt/ansibleapp -s /sbin/nologin -c "ansibleapp user" ansibleapp
RUN chown -R 1001:0 /opt/{ansible,ansibleapp}
USER 1001
