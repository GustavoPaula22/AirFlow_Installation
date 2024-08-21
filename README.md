# AirFlow_Installation

 - Instale o Ubunto pelo Microsoft Store e apos a instalacao

 - No PowerShell execute o seguinte comando para habilitar o WSL 
 * dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart

 - Reinicie a maquina, abra o app ubunto e deixe ele instalar e configurar seu distribution apos isso configure o user e pass unix de acesso
 
 - Atualize seu ambiente Linux
 * sudo apt update && sudo apt upgrade -y

 - Vamos instalar o Python e o pip
 * sudo apt install python3 python3-pip -y

 - Vamos criar o repositorio do AirFlow
 * export AIRFLOW_HOME=~/airflow
 * export PATH="$HOME/.local/bin:$PATH"
 * source ~/.bashrc  # ou ~/.zshrc
 * echo $PATH
   
 * AIRFLOW_VERSION=2.10.0
 * PYTHON_VERSION="$(python3 -c 'import sys; print(f"{sys.version_info.major}.{sys.version_info.minor}")')"
 * CONSTRAINT_URL="https://raw.githubusercontent.com/apache/airflow/constraints-${AIRFLOW_VERSION}/constraints-${PYTHON_VERSION}.txt"

 * pip3 install "apache-airflow==${AIRFLOW_VERSION}" --constraint "${CONSTRAINT_URL}"

 - Inicie o airflow
 * airflow standalone
