# ELK-stack + docker-compose + terraform + ansible + AWS example
This is a small example of ELK stack usage deployed to AWS cloud. For the purposes, I have used two t2.medium AWS EC2 instances, running linux installed with Docker and docker-compose. Instance 1st is running a python sanic web app + filebeat and 2nd instance is running ELK stack (Elasticsearch, Logstash, Kibana). The infrastructure provisioned + configured with terraform and ansible.

![image](https://user-images.githubusercontent.com/12199867/88908304-fbfff780-d259-11ea-98cb-73df8d78c003.png)
![image](https://user-images.githubusercontent.com/12199867/88908351-09b57d00-d25a-11ea-9616-e122b38b59ef.png)


### Description
Each folder contains `README.md` file how to launch the whole environment.

### Pre-install
```bash
$ pip install boto==2.49.0
$ ansible-galaxy install -r infra/ansible/requirements.yml
```

### Make usage

```bash
$ make help
help                           This help
terraform-init                 Init terraform project
terraform-plan                 Show terraform plan to apply
terraform-apply                Apply changes on infrastructure
ansible-setup                  Setup EC2 instances
elk-up                         Launch ELK stack
elk-down                       Stop ELK stack
echo-up                        Launch echo service + filebeat
echo-down                      Stop echo service + filebeat
clean-pyc                      Remove complied files
```

### Links
* https://www.elastic.co/guide/en/elasticsearch/reference/current/index.html
* https://www.elastic.co/guide/en/kibana/current/index.html
* https://www.elastic.co/guide/en/logstash/current/index.html
* https://www.elastic.co/guide/en/beats/libbeat/current/index.html
* https://www.elastic.co/guide/en/beats/filebeat/current/index.html
* https://www.elastic.co/guide/en/beats/metricbeat/current/index.html
* https://docs.docker.com/compose/compose-file/
* https://www.terraform.io/docs/configuration/index.html
* https://docs.ansible.com/ansible/latest/index.html
* https://docs.ansible.com/ansible/latest/user_guide/playbooks.html
* https://docs.ansible.com/ansible/latest/modules/modules_by_category.html
* https://galaxy.ansible.com/
* https://sanic.readthedocs.io/en/latest/
* https://pipenv.pypa.io/en/latest/
* https://www.uvicorn.org/
* https://docs.docker.com/compose/compose-file/
* https://aws.amazon.com/ec2/
