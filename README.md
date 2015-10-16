# bypass
weak password generation from china
## Installation

```
pip install xpinyin
git clone http://github.com/xl7dev/bypass.git
```
## Usage

```
Usage: bypass.py [options]

Options:
  -h, --help            show this help message and exit
  -u USERNAME, --username=USERNAME
                        username of target, split by "," or Space
  -g GENERATION, --generation=GENERATION
                        default generation china username Top500,default -g 1,
                        1->wangdachui,2->wang.dachui,3->wang.dc,4->dachui.wang
                        ,5->dc.wang,6->wdc,7->wangdc,8->wangdc1
  -f FILENAME, --filename=FILENAME
                        username lists
  -b BIRTHDAY, --birthday=BIRTHDAY
                        sfz format:341222200101011234 or birthday of target,
                        format: %Y%m%d
  -q QQ, --qq=QQ        QQ number of target, split by "," or Space
  -d DOMAIN, --domain=DOMAIN
                        domain of target, split by "," or Space
  -e EMAIL, --email=EMAIL
                        email of target, split by "," or Space
  -m MOBILE, --mobile=MOBILE
                        mobile phone/phone number of target, split by "," or
                        Space
  -r RANDOM, --random=RANDOM
                        generation random
  -v, --verbose         (optional) Print debug information.
```
每个参数都可以用","或者空格分割多个值，中文自动识别为英文，支撑1337匹配模式
## example

parameter | value
---|---
username | 张三,lisi
generation | 1-8
filename | filename.txt
birthday | 341222200101011234,20010101
QQ | 10086,1008611
domain | www.knownsec.com
email | admin@gmail.com
mobile | 13838438438
random | 8

### 企业公司
1.从文件名中加载多个用户名
```
python bypass.py -f username.txt -d www.knownsec.com
```
2.自动生成Top500用户名

```
python bypass.py -g 1 -d www.knownsec.com
```
### 个人
1.根据个人信息生成
```
bypass.py -f username.txt -b 20010101 -q 10086 -d www.knownsec.com -m 13838438438
```
