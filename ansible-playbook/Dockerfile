FROM python:3.7

RUN pip install 'ansible~=$ANSIBLE_VERSION'

ENV VAULT_PASSWORD=
ADD ansible.cfg /etc/ansible/ansible.cfg
ADD vault-password /usr/local/bin
WORKDIR /workspace

ENTRYPOINT ["ansible-playbook"]
