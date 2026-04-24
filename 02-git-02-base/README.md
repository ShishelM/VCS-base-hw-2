# Домашнее задание к занятию "`Основы Git`" - `Рыбянцев Павел`

------

*`немного переделал структуру репозитория, чтобы он  повторял структуру домашних заданий (для удобства)`

### Задание 1. Знакомимся с GitLab и Bitbucket

Настроил репозиторий GitLab по аналогии GitHub

результат команды `git remote -v`
```
gitlab  git@gitlab.com:ShishelM_lab/devops-netology.git (fetch)
gitlab  git@gitlab.com:ShishelM_lab/devops-netology.git (push)
origin  git@github.com:ShishelM/devops-netology.git (fetch)
origin  git@github.com:ShishelM/devops-netology.git (push)
```
Выполните push локальной ветки `main`
```
# Локальный
pavel@ubuntu-24:~/devops-netology$ git log -1 --format="%H"
2793c57b0c2f8511541f913fedbdf621a82211cc

# GitHub
pavel@ubuntu-24:~/devops-netology$ git ls-remote --heads origin main
2793c57b0c2f8511541f913fedbdf621a82211cc        refs/heads/main

# GitLab
pavel@ubuntu-24:~/devops-netology$ git ls-remote --heads gitlab main
2793c57b0c2f8511541f913fedbdf621a82211cc        refs/heads/main

# Проверка что послежний коммит везде совпадает
pavel@ubuntu-24:~/devops-netology$ git log --oneline --graph --all
* 2793c57 (HEAD -> main, origin/main, gitlab/main) Fix: readme
* d4e5e81 Fix: readme amd img
* 6a91b0b Fix: convert submodule to normal folder with files
* dc92e1e Final fix: proper folder structure
```