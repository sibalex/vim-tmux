### readme.txt
#Создаем папку под новый проект
mkdir ~/Code/{newproject}
cd ~/Code/{newproject}

#Установка env https://stackoverflow.com/questions/24123150/pyvenv-3-4-returned-non-zero-exit-status-1
python3.8 -m venv env

#Активация
. ./env/bin/activate

#Дальше можно устанавливать пакеты из requirements.txt #pip freeze > requirements.txt
pip install -r requirements.txt

#Как альтертнатива conda из anaconda3
conda create -n {myenv} python=3.8
conda env list
conda activate {myenv}
pip install {}
conda deactivate

#alias .zshrc
alias IDE="source /Users/alexander/opt/anaconda3/bin/activate && conda activate scientific && conda env list && python --version"

#help conda
https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf

# с .git
1. создать папку для работы
2. на гите должна быть созданный репозиторий
3. в созданной папке проекта в терминале (дается на git при создании нового проекта):
    git init
    git add README.md
    git commit -m "first commit"
    git remote add origin git@github.com:{name}.git
    git push -u origin master

    git clone git@github.com:{name}.git
4. virtualenv env --python=python3   # или указать версию.  (virtualenv --python=/usr/bin/python3.4 venv)
5. создать requirements.txt и прописать необходимые модули (пример:"""numpy pandas matplotlib seaborn""")
6. . ./env/bin/activate 
# пример по конде: (source /Users/alexander/opt/anaconda3/bin/activate && conda activate scientific)
7. pip install -r requirements.txt



### requirements.txt
requests
bs4
numpy
pandas
matplotlib
scikit-learn
