ansible-playbook -i hosts install-docker.yml --ask-become-pass
ansible-playbook -i hosts install-minikube.yml --ask-become-pass
ansible-playbook -i hosts install-jenkins.yml --ask-become-pass
