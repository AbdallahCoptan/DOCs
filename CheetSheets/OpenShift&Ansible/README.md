[mrxpalmeiras](https://sites.google.com/site/mrxpalmeiras/)
-----------------------------------------------------------

Search this site

+--------------------------------------+--------------------------------------+
| #### Navigation {.sites-embed-title} | [Ansible](/site/mrxpalmeiras/ansible |
|                                      | )‎                                   |
| -   [Ansible](/site/mrxpalmeiras/ans | \> ‎                                 |
| ible)                                | ### Ansible Cheat Sheet {#sites-page |
| -   [AWS](/site/mrxpalmeiras/aws-che | -title-header xmlns="http://www.w3.o |
| atsheet)                             | rg/1999/xhtml" style="" align="left" |
| -   [Docker](/site/mrxpalmeiras/dock | }                                    |
| er)                                  |                                      |
| -   [Crystal](/site/mrxpalmeiras/cry | +----------------------------------- |
| stal-cheatsheet)                     | ------------------------------------ |
| -   [Elastic](/site/mrxpalmeiras/ela | ---+                                 |
| stic-cheatsheet)                     | | +--------------------------------- |
| -   [FiSH](/site/mrxpalmeiras/notes/ | -----+------------------------------ |
| fish)                                | -- |                                 |
| -   [Git](/site/mrxpalmeiras/git)    | | ------+                            |
| -   [Golang](/site/mrxpalmeiras/gola |                                      |
| ng)                                  |    |                                 |
| -   [JavaScript](/site/mrxpalmeiras/ | | | ![](https://sites.google.com/sit |
| javascript-jquery)                   | e/mr | Contents                      |
| -   [Linux](/site/mrxpalmeiras/linux |    |                                 |
| )                                    | |       |                            |
| -   [Puppet](/site/mrxpalmeiras/pupp |                                      |
| et)                                  |    |                                 |
| -   [Python](/site/mrxpalmeiras/pyth | | | xpalmeiras/_/rsrc/1514392856390/ |
| on)                                  | ansi |                               |
| -   [Ruby](/site/mrxpalmeiras/ruby)  |    |                                 |
| -   [SaltStack](/site/mrxpalmeiras/s | |       |                            |
| altstack)                            |                                      |
| -   [More...](/site/mrxpalmeiras/not |    |                                 |
| es)                                  | | | ble/ansible-cheat-sheet/ansible. |
| -   [Scratchpad](/site/mrxpalmeiras/ | png? | 1.  [**1**SSH Setup](#TOC-SSH |
| scratchpad)                          | -S |                                 |
| -   [Ninja                           | | etup) |                            |
|     Tools](/site/mrxpalmeiras/ninjat |                                      |
| ools)                                |    |                                 |
|                                      | | | height=200&width=200)            |
|                                      |      | 2.  [**2**REMOTE CMD (Ad      |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      |     Hoc)](#TOC-REMOTE-CMD-Ad- |
|                                      | Ho |                                 |
|                                      | | c-)   |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | 3.  [**3**SERVER              |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      |     DIAGNOSTICS](#TOC-SERVER- |
|                                      | DI |                                 |
|                                      | | AGNOS |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | TICS)                         |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | 4.  [**4**PACKAGES AND        |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      |     INSTALLATION](#TOC-PACKAG |
|                                      | ES |                                 |
|                                      | | -AND- |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | INSTALLATION)                 |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | 5.  [**5**JOBS AND PROCESS    |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      |     CONTROL](#TOC-JOBS-AND-PR |
|                                      | OC |                                 |
|                                      | | ESS-C |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | ONTROL)                       |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | 6.  [**6**CONDITIONALS](#TOC- |
|                                      | CO |                                 |
|                                      | | NDITI |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | ONALS)                        |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | 7.  [**7**VARIABLES](#TOC-VAR |
|                                      | IA |                                 |
|                                      | | BLES) |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      |     1.  [**7.1**Variables ins |
|                                      | id |                                 |
|                                      | | e     |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      |         Inventory Hosts       |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      |         file](#TOC-Variables- |
|                                      | in |                                 |
|                                      | | side- |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | Inventory-Hosts-file)         |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | 8.  [**8**MODULES](#TOC-MODUL |
|                                      | ES |                                 |
|                                      | | )     |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | 9.  [**9**GALAXY](#TOC-GALAXY |
|                                      | )  |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | 10. [**10**PLAYBOOKS](#TOC-PL |
|                                      | AY |                                 |
|                                      | | BOOKS |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | )                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | 11. [**11**USER AND GROUP     |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      |     MGMT](#TOC-USER-AND-GROUP |
|                                      | -M |                                 |
|                                      | | GMT)  |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | 12. [**12**FILES &            |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      |     DIRS](#TOC-FILES-DIRS)    |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | 13. [**13**FACTER](#TOC-FACTE |
|                                      | R) |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | +--------------------------------- |
|                                      | -----+------------------------------ |
|                                      | -- |                                 |
|                                      | | ------+                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | |                                    |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | \                                  |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | +--------------------------------- |
|                                      | -----+------------------------------ |
|                                      | -- |                                 |
|                                      | | ------+                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | **SSH Setup**                    |
|                                      |      | **GALAXY**                    |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | -------------                    |
|                                      |      | ----------                    |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | **\                              |
|                                      |      | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | **                               |
|                                      |      |  install Role (Module)        |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | Copy your Ansible Master's publi |
|                                      | c    | `ansible-galaxy install geerl |
|                                      | in |                                 |
|                                      | | gguy. |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | key to the managed node          |
|                                      |      | nginx`                        |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `ssh-keygen  ## generate public  |
|                                      | key` | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `ssh-copy-id <name of node>  # c |
|                                      | opy  | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | key, provide password to node`   |
|                                      |      | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | configure Hosts file             |
|                                      |      | * * * * *                     |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `/etc/ansible/hosts`             |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `[production]`                   |
|                                      |      | **PLAYBOOKS**                 |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `prod1.prod.local`               |
|                                      |      | -------------                 |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `prod2.prod.local`               |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      | run playbook with sudo        |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `[dev]`                          |
|                                      |      | `ansible-playbook -v config-u |
|                                      | se |                                 |
|                                      | | rs.ya |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `devweb1.dev.local`              |
|                                      |      | ml --sudo --sudo-user=joe --a |
|                                      | sk |                                 |
|                                      | | -sudo |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `devweb2.dev.local`              |
|                                      |      | -pass`                        |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | * * * * *                        |
|                                      |      | use different Hosts file      |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | `ansible-playbook -v -i /path |
|                                      | /t |                                 |
|                                      | | o/hos |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | **REMOTE CMD (Ad Hoc)**          |
|                                      |      | ts `                          |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | -----------------------          |
|                                      |      | ``                            |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | run playbook but only a speci |
|                                      | fi |                                 |
|                                      | | c     |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      | task (tag)                    |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  Ping specific node              |
|                                      |      | `ansible-playbook playbooks/r |
|                                      | es |                                 |
|                                      | | tore_ |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `ansible -i hosts nycweb01.prod. |
|                                      | loca | bitbucket.yaml  -i hosts --ta |
|                                      | gs |                                 |
|                                      | |  rsyn |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | l -m ping`                       |
|                                      |      | c   or to skip: (--skip-tags  |
|                                      | ta |                                 |
|                                      | | g1, t |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      | ag2)`\                        |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  Ping with wildcard              |
|                                      |      | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `ansible -i hosts "nycweb*" -m p |
|                                      | ing` | store output of a command as  |
|                                      | a  |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      | variable\                     |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | Ping all nodes with SSH user 'ro |
|                                      | ot'\ |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  ansible -i hosts all -m ping -u |
|                                      |      | `shell: cat /etc/network | gr |
|                                      | ep |                                 |
|                                      | |  eth0 |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | root\                            |
|                                      |      | `\                            |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  \                               |
|                                      |      |  `register: address`          |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  run a command                   |
|                                      |      | `debug: msg="address is {{ ad |
|                                      | dr |                                 |
|                                      | | ess.s |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `ansible -i hosts dev -a 'uname  |
|                                      | -a'` | tdout }}"`                    |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | check Yum packages               |
|                                      |      | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `ansible -i hosts dev -m yum `   |
|                                      |      | configure multiple items with |
|                                      |  o |                                 |
|                                      | | ne    |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      | task                          |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  check if Docker rpm is installe |
|                                      | d    | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ansible -i hosts web01.nyc.local |
|                                      |  -m  | `- name: more complex items t |
|                                      | o  |                                 |
|                                      | | add s |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | shell -a "rpm -qa | grep docker" |
|                                      |      | everal users`                 |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      | `  user:`                     |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | Get facts about a box            |
|                                      |      | `    name: "{{ item.name }}"` |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `ansible -i hosts web01.nyc.loca |
|                                      | l -m | `    uid: "{{ item.uid }}"`   |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  setup -a 'filter=facter_*'`\    |
|                                      |      | `    groups: "{{ item.groups  |
|                                      | }} |                                 |
|                                      | | "`    |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  \                               |
|                                      |      | `    state: present`          |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  run command with sudo           |
|                                      |      | `  with_items:`               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `ansible -i hosts target-host -m |
|                                      |  she | `     - { name: testuser1, ui |
|                                      | d: |                                 |
|                                      | |  1002 |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ll -a "cat /etc/sudoers" --sudo  |
|                                      | `    | , groups: "wheel, staff" }`   |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      | `     - { name: testuser2, ui |
|                                      | d: |                                 |
|                                      | |  1003 |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | limit command to a certain group |
|                                      |  or  | , groups: staff }`            |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | server: add --limit \*.nyc       |
|                                      |      | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      | get path location of current  |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      | Playbook (pwd)\               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      | ``` {style="margin-top:0px;ma |
|                                      | rg |                                 |
|                                      | | in-bo |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      | ttom:1em;padding:5px;border:0 |
|                                      | px |                                 |
|                                      | | ;font |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      | -stretch:inherit;line-height: |
|                                      | in |                                 |
|                                      | | herit |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | ;vertical-align:baseline;widt |
|                                      | h: |                                 |
|                                      | | auto; |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | * * * * *                        |
|                                      |      | max-height:600px;overflow:aut |
|                                      | o; |                                 |
|                                      | | word- |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | wrap:normal"}                 |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | **SERVER DIAGNOSTICS**           |
|                                      |      | {{ playbook_dir }}            |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ----------------------           |
|                                      |      | Set playbook to be verbose by |
|                                      |  d |                                 |
|                                      | | efaul |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | t                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      | - hosts: blah                 |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  Test Connection\                |
|                                      |      |   strategy: debug             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  ansible -i hosts all -m ping -u |
|                                      |      | ```                           |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | root**\                          |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  \                               |
|                                      |      | run playbook with verbose tra |
|                                      | ce |                                 |
|                                      | | back  |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ****Diagnostics**\               |
|                                      |      | `ansible-playbook -i hosts my |
|                                      | Pl |                                 |
|                                      | | ayboo |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  \                               |
|                                      |      | k.yaml -vvv`                  |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  \                               |
|                                      |      | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  \                               |
|                                      |      | run playbook on multiple Host |
|                                      |  g |                                 |
|                                      | | roups |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  manage nodes via                |
|                                      |      | - hosts: "search\_head, deplo |
|                                      | ye |                                 |
|                                      | | r"    |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | "/etc/ansible/hosts" file        |
|                                      |      | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      | Run playbook locally on host\ |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | Debug (debug output for playbook |
|                                      | )    |  \                            |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `- debug: var=result verbosity=2 |
|                                      |   `  | `hosts: 127.0.0.1`\           |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      |  ` connection: local`         |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | * * * * *                        |
|                                      |      |  Prompt for password during P |
|                                      | la |                                 |
|                                      | | ybook |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | run                           |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | **PACKAGES AND INSTALLATION**    |
|                                      |      | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | -----------------------------    |
|                                      |      | `# Playbook to change user pa |
|                                      | ss |                                 |
|                                      | | word  |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | `                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | **\                              |
|                                      |      | `- name: pw change`\          |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | **                               |
|                                      |      |  `  hosts: target`\           |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | install multiple packages\       |
|                                      |      |  `  become: true`\            |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `yum: name="{{ item }}" state=pr |
|                                      | esen | `  become_user: root   vars_p |
|                                      | ro |                                 |
|                                      | | mpt:  |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | t `\                             |
|                                      |      |     - name: username       pr |
|                                      | om |                                 |
|                                      | | pt: " |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  `with_items:`\                  |
|                                      |      | enter username for which to c |
|                                      | ha |                                 |
|                                      | | nge t |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  `  - http `\                    |
|                                      |      | he pw"     - name: password   |
|                                      |    |                                 |
|                                      | |    pr |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  `  - htop`\                     |
|                                      |      | ompt: "enter new password"    |
|                                      |    |                                 |
|                                      | |   pri |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  `  - myapp`                     |
|                                      |      | vate: yes      tasks:     - n |
|                                      | am |                                 |
|                                      | | e: ch |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | **\                              |
|                                      |      | ange pw       user: "name={{  |
|                                      | us |                                 |
|                                      | | ernam |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | **                               |
|                                      |      | e }} password={{ password }}  |
|                                      | up |                                 |
|                                      | | date_ |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | **\                              |
|                                      |      | password=always"    `         |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | **                               |
|                                      |      | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | **\                              |
|                                      |      |  run playbook with "dry run"  |
|                                      | /  |                                 |
|                                      | | NOOP  |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | **                               |
|                                      |      | / simulate\                   |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      |     ansible-playbook foo.yml  |
|                                      | -- |                                 |
|                                      | | check |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | * * * * *                        |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | **JOBS AND PROCESS CONTROL**     |
|                                      |      | Run task on different target, |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ----------------------------     |
|                                      |      | `- name: run something on som |
|                                      | e  |                                 |
|                                      | | other |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      |  server`                      |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | run Ansible ad hoc with 10 paral |
|                                      | lel  | `  debug: msg="running stuff" |
|                                      | `  |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | forks \                          |
|                                      |      | `  delegate_to: someserver`\  |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `ansible -i hosts testnode1 -a " |
|                                      | unam | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | e -a" -f 10`                     |
|                                      |      | Delegate task to a host group |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      | `- name: restart web servers  |
|                                      | `\ |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | show human readable output\      |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | add this line to ansible.cfg\    |
|                                      |      | `  service: name=memcached st |
|                                      | at |                                 |
|                                      | | e=res |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `stdout_callback=yaml`           |
|                                      |      | tarted `\                     |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      |  `  delegate_to: "{{ item }}" |
|                                      | `\ |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | * * * * *                        |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | `  with_items: "{{ groups['we |
|                                      | bs |                                 |
|                                      | | erver |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | **CONDITIONALS**                 |
|                                      |      | s'] }}"`                      |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ----------------                 |
|                                      |      | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | Get IP or facter of a remote  |
|                                      | ho |                                 |
|                                      | | st    |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | y file to n                      |
|                                      |      | `- name: get IP`              |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      | `  debug: msg="{{ hostvars['n |
|                                      | yc |                                 |
|                                      | | web01 |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      | ']['ansible_default_ipv4']['a |
|                                      | dd |                                 |
|                                      | | ress' |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      | ] }}"`                        |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | * * * * *                        |
|                                      |      | or \                          |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      |  \                            |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | **VARIABLES**                    |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | -------------                    |
|                                      |      | `debug: msg="{{ hostvars[item |
|                                      | ][ |                                 |
|                                      | | 'ansi |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | ble_ssh_host'] }}"`\          |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | **include global variables for a |
|                                      | ll   | `with_items: "{{ groups['webs |
|                                      | er |                                 |
|                                      | | vers' |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | Roles**\                         |
|                                      |      | ] }}"`                        |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  \                               |
|                                      |      | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | sample playbook                  |
|                                      |      | synchronize file (copy file f |
|                                      | ro |                                 |
|                                      | | m     |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ``` {style="margin-top:0px;margi |
|                                      | n-bo | Ansible host to target)       |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ttom:1em;padding:5px;border:0px; |
|                                      | font |   `- synchronize: `           |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | -stretch:inherit;line-height:inh |
|                                      | erit | `     src: "{{ playbook_dir } |
|                                      | }/ |                                 |
|                                      | | files |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ;font-family:Consolas,Menlo,Mona |
|                                      | co,L | /vscode.repo"`                |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ucida Console,Liberation Mono,De |
|                                      | jaVu | `     dest: /etc/yum.repos.d/ |
|                                      |  ` |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  Sans Mono,Bitstream Vera Sans M |
|                                      | ono, | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | Courier New,monospace,sans-serif |
|                                      | ;ver | synchronize from server A to  |
|                                      | se |                                 |
|                                      | | rver  |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | tical-align:baseline;width:auto; |
|                                      | max- | B with a wildcard             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | height:600px;overflow:auto;backg |
|                                      | roun | `    - name: copy Splunk Apps |
|                                      | `  |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | d-color:rgb(239,240,241);word-wr |
|                                      | ap:n | `      synchronize:         s |
|                                      | rc |                                 |
|                                      | | : "/o |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ormal;color:rgb(36,39,41)"}      |
|                                      |      | pt/splunk/etc/apps/{{ item }} |
|                                      | "  |                                 |
|                                      | | (serv |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | splunk/                          |
|                                      |      | er A)`                        |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |    setup_splunk_playbook.yaml    |
|                                      |      | `        dest: "/opt/splunk/e |
|                                      | tc |                                 |
|                                      | | /shcl |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |    roles/base                    |
|                                      |      | uster/apps/"  (server B)`     |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |            /tasks/main.yaml      |
|                                      |      | `      with_items:        - i |
|                                      | te |                                 |
|                                      | | m1    |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |            /tasks/install.yaml   |
|                                      |      |      - item2`                 |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |          search_head             |
|                                      |      | `      delegate_to: server A` |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |            /tasks/configure.yaml |
|                                      |      | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |          indexer                 |
|                                      |      | wget a file to a location     |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |            /tasks/configure.yaml |
|                                      |      | `  - get_url:`                |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |          some_other_role         |
|                                      |      | `      url: 'https://dl.googl |
|                                      | e. |                                 |
|                                      | | com/g |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |            /tasks/some_task.yaml |
|                                      |      | o/go1.10.linux-amd64.tar.gz'  |
|                                      | `  |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |    hosts                         |
|                                      |      | `      dest: '/tmp'      forc |
|                                      | e: |                                 |
|                                      | |  no   |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |    config.yaml                   |
|                                      |      | # dont download if file alrea |
|                                      | dy |                                 |
|                                      | |  exis |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ```                              |
|                                      |      | ts`                           |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | ``                            |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | Place your vars into config.yaml |
|                                      |      | `untar tar.gz`                |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | *cat splunk/config.yaml*         |
|                                      |      | * * * * *                     |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ``` {style="margin-top:0px;margi |
|                                      | n-bo | **USER AND GROUP MGMT**       |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ttom:1em;padding:5px;border:0px; |
|                                      | font | -----------------------       |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | -stretch:inherit;line-height:inh |
|                                      | erit |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ;font-family:Consolas,Menlo,Mona |
|                                      | co,L | **\                           |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ucida Console,Liberation Mono,De |
|                                      | jaVu | **                            |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  Sans Mono,Bitstream Vera Sans M |
|                                      | ono, | change user password for user |
|                                      |  J |                                 |
|                                      | | oe    |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | Courier New,monospace,sans-serif |
|                                      | ;ver | (user Fred running the cmd as |
|                                      |  s |                                 |
|                                      | | udo   |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | tical-align:baseline;width:auto; |
|                                      | max- | on the target box)            |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | height:600px;overflow:auto;backg |
|                                      | roun | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | d-color:rgb(239,240,241);word-wr |
|                                      | ap:n |  \# 1 install passlib \       |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ormal;color:rgb(36,39,41)"}      |
|                                      |      |  `pip install passlib`\       |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ---                              |
|                                      |      |  \                            |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | # global Splunk variables        |
|                                      |      |  \#2 update the pw, using a h |
|                                      | as |                                 |
|                                      | | h\    |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | splunk_version: 7.0.0            |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ```                              |
|                                      |      | `ansible targethost -s -m use |
|                                      | r  |                                 |
|                                      | | -a "n |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | ame=joe update_password=alway |
|                                      | s  |                                 |
|                                      | | passw |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | in your playbook, include the Ro |
|                                      | les  | ord={{ 'MyNewPassword' | pass |
|                                      | wo |                                 |
|                                      | | rd_ha |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | sh('sha512') }}" -u fred --as |
|                                      | k- |                                 |
|                                      | | sudo- |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | *cat setup\_splunk\_playbook.yam |
|                                      | l*   | pass`{style="color:rgb(0,96,0 |
|                                      | )" |                                 |
|                                      | | }     |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ``` {style="margin-top:0px;margi |
|                                      | n-bo |  copy public ssh key to remot |
|                                      | e  |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ttom:1em;padding:5px;border:0px; |
|                                      | font | authorized\_keys file         |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | -stretch:inherit;line-height:inh |
|                                      | erit |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ;font-family:Consolas,Menlo,Mona |
|                                      | co,L | `- hosts: targetHost`  tasks: |
|                                      | \  |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ucida Console,Liberation Mono,De |
|                                      | jaVu |        - name: update nessus  |
|                                      | SS |                                 |
|                                      | | H     |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  Sans Mono,Bitstream Vera Sans M |
|                                      | ono, | keys\                         |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | Courier New,monospace,sans-serif |
|                                      | ;ver |          become\_user: root\  |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | tical-align:baseline;width:auto; |
|                                      | max- |          become\_method: sudo |
|                                      | \  |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | height:600px;overflow:auto;backg |
|                                      | roun |          become: true\        |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | d-color:rgb(239,240,241);word-wr |
|                                      | ap:n |          authorized\_key:\    |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ormal;color:rgb(36,39,41)"}      |
|                                      |      |             user: nessus\     |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | - hosts: "search_heads"          |
|                                      |      |             key: "{{          |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |   become_user: root              |
|                                      |      | lookup('pipe','cat            |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |   become: true                   |
|                                      |      | ../files/ssh\_keys/nessus.pub |
|                                      | ') |                                 |
|                                      | |  }}"\ |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |   gather_facts: true             |
|                                      |      |             state: present    |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |   roles:                         |
|                                      |      | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |     - base                       |
|                                      |      | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |     - search_head                |
|                                      |      | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ```                              |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | * * * * *                     |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | in your Role, include the Global |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | Vars inside a Task               |
|                                      |      | **FILES & DIRS**              |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | ----------------              |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | *cat roles/base/tasks/main.yaml* |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | delete all files and hidden f |
|                                      | il |                                 |
|                                      | | es in |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ``` {style="margin-top:0px;margi |
|                                      | n-bo | a directory                   |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ttom:1em;padding:5px;border:0px; |
|                                      | font | `vars:   app_home: /var/opt/a |
|                                      | pp |                                 |
|                                      | | licat |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | -stretch:inherit;line-height:inh |
|                                      | erit | ion  tasks:   - name: clear h |
|                                      | om |                                 |
|                                      | | e dir |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ;font-family:Consolas,Menlo,Mona |
|                                      | co,L | `\                            |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ucida Console,Liberation Mono,De |
|                                      | jaVu |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  Sans Mono,Bitstream Vera Sans M |
|                                      | ono, | `  - shell: "ls -la {{ app_ho |
|                                      | me |                                 |
|                                      | |  }}/" |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | Courier New,monospace,sans-serif |
|                                      | ;ver | `\                            |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | tical-align:baseline;width:auto; |
|                                      | max- |  `    register: files_to_dele |
|                                      | te |                                 |
|                                      | | `\    |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | height:600px;overflow:auto;backg |
|                                      | roun |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | d-color:rgb(239,240,241);word-wr |
|                                      | ap:n | `  - file: path="{{ app_home  |
|                                      | }} |                                 |
|                                      | | /{{ i |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ormal;color:rgb(36,39,41)"}      |
|                                      |      | tem }}" state=absent`\        |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ---                              |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | # install Splunk Base            |
|                                      |      | `    with_items: "{{ files_to |
|                                      | _d |                                 |
|                                      | | elete |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | .stdout_lines }}"`            |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | - name: include vars             |
|                                      |      | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |   include_vars: "{{ playbook_dir |
|                                      |  }}/ | get files from node           |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | config.yaml"                     |
|                                      |      | `ansible node1 -s -m fetch -a |
|                                      |  " |                                 |
|                                      | | src=/ |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | etc/hosts dest=/tmp"`         |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | - include: install.yaml          |
|                                      |      | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ```                              |
|                                      |      | copy file to node             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | `ansible node1 -m copy -a "sr |
|                                      | c= |                                 |
|                                      | | /etc/ |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | vars are accessible in tasks now |
|                                      | ,    | hosts  dest=/tmp/hosts"`      |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | cat roles/base/tasks/install.yam |
|                                      | l    | remove all files matching a w |
|                                      | il |                                 |
|                                      | | dcard |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | `file: path={{ item }} state= |
|                                      | ab |                                 |
|                                      | | sent` |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ``` {style="margin-top:0px;margi |
|                                      | n-bo | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ttom:1em;padding:5px;border:0px; |
|                                      | font | `with_fileglob: /tmp/*.rpm`   |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | -stretch:inherit;line-height:inh |
|                                      | erit | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ;font-family:Consolas,Menlo,Mona |
|                                      | co,L |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ucida Console,Liberation Mono,De |
|                                      | jaVu | * * * * *                     |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  Sans Mono,Bitstream Vera Sans M |
|                                      | ono, |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | Courier New,monospace,sans-serif |
|                                      | ;ver | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | tical-align:baseline;width:auto; |
|                                      | max- | **FACTER**                    |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | height:600px;overflow:auto;backg |
|                                      | roun | ----------                    |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | d-color:rgb(239,240,241);word-wr |
|                                      | ap:n |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ormal;color:rgb(36,39,41)"}      |
|                                      |      | get all facts from a node (ad |
|                                      |  h |                                 |
|                                      | | oc)   |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | - name: echo version             |
|                                      |      | `ansible -i hosts targetName  |
|                                      | -m |                                 |
|                                      | |  setu |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |   debug: splunk version is {{ sp |
|                                      | lunk | p -a "filter="facter_*"`      |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | _version }}                      |
|                                      |      | ``                            |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ```                              |
|                                      |      | use fact in a playbook\       |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      |  include fact as {{           |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      | ansible\_factname }}          |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | **Loop through a Dict variable   |
|                                      |      | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | inside a playbook**              |
|                                      |      | add fact to Hosts file\       |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      |  `[group]`\                   |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  cluster:                        |
|                                      |      |  `host1 admin_user=jane`\     |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |   members:                       |
|                                      |      |  `host2 admin_user=jack`\     |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |     splunk01: 10.123.1.0         |
|                                      |      |  `host3 `\                    |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |     splunk02: 10.123.1.1         |
|                                      |      |  \                            |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |     splunk03: 10.123.1.2\        |
|                                      |      |  `[group:vars] `\             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  \                               |
|                                      |      |  `admin_user=john`            |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  in the playbook, \              |
|                                      |      | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | get default IPV4 address      |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `- debug: msg="{{ cluster.member |
|                                      | s.va | `ansible_default_ipv4.address |
|                                      | `  |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | lues() | map('regex_replace', '( |
|                                      | .*)' | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | , 'https://\\1:8089') | join(',' |
|                                      | ) }} | **Local facts\                |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | "`\                              |
|                                      |      |  \                            |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  \                               |
|                                      |      | **                            |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      | `place `**`.``fact`**` file i |
|                                      | nt |                                 |
|                                      | | o /et |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `>> https://10.123,1.0:8089, htt |
|                                      | ps:/ | c/ansible/facts.d on target n |
|                                      | od |                                 |
|                                      | | e`    |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | /10.123.1.1:8089, etc etc`       |
|                                      |      | `vim /etc/ansible/facts.d/fru |
|                                      | it |                                 |
|                                      | | s.fac |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      | t`                            |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | **Use Inventory file variables   |
|                                      |      | `[fruits]`                    |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | inside a playbook\               |
|                                      |      | `sweet=banana, apple, grapes` |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | **\                              |
|                                      |      | `bitter=grapefruit`           |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | cat hosts                        |
|                                      |      | \                             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `[apache]`                       |
|                                      |      | `get Local facts`             |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `nycweb01`                       |
|                                      |      | `ansible -i hosts mrx -m setu |
|                                      | p  |                                 |
|                                      | | -a "f |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      | ilter=ansible_local"`         |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | playbook                         |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `debug: msg="IP: ``{{ hostvars[g |
|                                      | roup |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | s['apache'][0]]['ansible_default |
|                                      | _ipv |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | 4']['address'] }}"`              |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `debug: msg="Hostname: ``{{ host |
|                                      | vars |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | [groups['apache'][0]]['inventory |
|                                      | _hos |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | tname'] }}"`                     |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | register a List/Array to be used |
|                                      |  for |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | later,                           |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `- name: parse all hostnames in  |
|                                      | grou |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | p WebServer  and get their IPs,  |
|                                      | plac |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | e them in a list`                |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `  command: echo {{ hostvars[ite |
|                                      | m][' |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ansible_ssh_host'] }}"`          |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `  with_items: "{{ groups['webse |
|                                      | rver |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | '] }}"`                          |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `  register: ip_list`\           |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  \                               |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  `- name: show the IPs`          |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `  debug: msg={{ ip_list.results |
|                                      |  | m |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ap(attribute='item') | list }}"` |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | export an Environment variable   |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `- name: yum install`\           |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `  yum: name=somepkg state=prese |
|                                      | nt`\ |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `  environment: `\               |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `    SOME_VAR: abc`              |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | #### Variables inside Inventory  |
|                                      | Host |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | s file                           |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | cat hosts                        |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `[web]`                          |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `nycweb01.company.local`\        |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `[web:vars]`                     |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `role="super duper web server"`  |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | now get the "role" variable insi |
|                                      | de   |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | the playbook,                    |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `- hosts: web`\                  |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `  gather_facts: true`\          |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `  tasks:`\                      |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `    - name: print Role var`     |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `      debug: msg={{ role }}`\   |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `// super duper web server`\     |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |   \                              |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | * * * * *                        |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | MODULES                          |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | -------                          |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |                                  |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | **`service`**`: name=httpd state |
|                                      | =[st |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | arted, stopped, restarted, reloa |
|                                      | ded] |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | |  enabled=[yes,no]`               |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | **`user`**`: name=joe state=[pre |
|                                      | sent |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ,absent] uid=1001 groups=wheel s |
|                                      | hell |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | =/bin/bash`                      |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | `group: name=splunk gid=6600 sta |
|                                      | te=[ |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | present,absent] system=[yes/no]` |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | **`yum`**`: name=apache state=[p |
|                                      | rese |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | nt, latest, absent, removed]  `  |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | **`file`**`: path=/etc/file stat |
|                                      | e=[f |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | ile, link, directory, hard, touc |
|                                      | h, a |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | bsent] group=x owner=x recurse=y |
|                                      | es`  |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | | \                                |
|                                      |      |                               |
|                                      |    |                                 |
|                                      | |       |                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | +--------------------------------- |
|                                      | -----+------------------------------ |
|                                      | -- |                                 |
|                                      | | ------+                            |
|                                      |                                      |
|                                      |    |                                 |
|                                      | |                                    |
|                                      |                                      |
|                                      |    |                                 |
|                                      | | \                                  |
|                                      |                                      |
|                                      |    |                                 |
|                                      | +----------------------------------- |
|                                      | ------------------------------------ |
|                                      | ---+                                 |
|                                      |                                      |
|                                      | Comments                             |
+--------------------------------------+--------------------------------------+

my stuff
 [https://github.com/perfecto25/](https://github.com/perfecto25/)

[Sign
in](https://accounts.google.com/ServiceLogin?continue=https://sites.google.com/site/mrxpalmeiras/ansible/ansible-cheat-sheet&service=jotspot)|[Recent
Site
Activity](/site/mrxpalmeiras/system/app/pages/recentChanges)|[Report
Abuse](https://sites.google.com/site/mrxpalmeiras/system/app/pages/reportAbuse)|[Print
Page](javascript:;)|Powered By **[Google
Sites](http://sites.google.com/site)**
