import requests
from user_agent import generate_user_agent
import os
import datetime
from uuid import uuid4
uid = str(uuid4())
import random
os.system('clear')
B="\033[1;30m" # Black
R="\033[1;31m" # Red
G="\033[1;32m" # Green
Y="\033[1;33m" # Yellow
Bl="\033[1;34m" # Blue
P="\033[1;35m" # Purple
C="\033[1;36m" # Cyan
W="\033[1;37m" # White
H="\x1b[38;5;208m" #
M = '\x1b[1;37m' 

	   
                       

gg = 0
listoo = ['HI']    
            
linux = 'clear'
windows = 'cls'
print('') 
username = str(input(f"{H} «: يــــوزر حسابك الوهمي [=]{C}"))
print('')
password = str(input(f"{H}   «: باسورد حسابك الوهمي [=]{C}"))
print('')
[linux, windows][os.name == 'nt']
url ='https://b.i.instagram.com/api/v1/accounts/login/'
headers = {'User-Agent': 'Instagram 113.0.0.39.122 Android (24/5.0; 515dpi; 1440x2416; huawei/google; Nexus 6P; angler; angler; en_US)'}
  
  
data = {
  'uuid':uid, 
  'password':password, 
  'username':username, 
  'device_id':uid, 
  'from_reg':'false', 
  '_csrftoken':'missing', 
  'login_attempt_countn':'0'
 }		
k = requests.post(url,headers=headers,data=data)
if ('"logged_in_user"') in  k.text or 'userId' in k.text:
	print(f"{Y} تسجيل دخول ناجح✔️")
	print('')
	
	([linux, windows][os.name == 'nt'])
	sessionid = k.cookies['sessionid']

user = str(input(f"{H}    «: يوزر تسحب منه لسته [=]{C}"))
gg = 0
listoo = ['HI']
def fg(id):
    global gg
    url = f'https://i.instagram.com/api/v1/friendships/{id}/following/?count=200'
    headers = {
        'Accept': '*/*',
        'Accept-Encoding': 'gzip, deflate, br',
        'Accept-Language': 'en-US,en;q=0.9',
        'Cookie': f'mid=Y3bGYwALAAHNwaKANMB8QCsRu7VA; ig_did=092BD3C7-0BB2-414B-9F43-3170EAED8778; ig_nrcb=1; shbid=1685054; shbts=1675191368.6684434090; rur=CLN; ig_direct_region_hint=ATN; csrftoken=gLlFX76z8qqwDgmh8ZIp3uFhAeX4zKdO; ds_user_id=921803283; sessionid={sessionid}',
        'Sec-Ch-Prefers-Color-Scheme': 'dark',
        'Sec-Ch-Ua': '"Not.A/Brand";v="8", "Chromium";v="114", "Microsoft Edge";v="114"',
        'Sec-Ch-Ua-Full-Version-List': '"Not.A/Brand";v="8.0.0.0", "Chromium";v="114.0.5735.201", "Microsoft Edge";v="114.0.1823.67"',
        'Sec-Ch-Ua-Mobile': '?0',
        'Sec-Ch-Ua-Platform': '"Windows"',
        'Sec-Ch-Ua-Platform-Version': '"15.0.0"',
        'Sec-Fetch-Dest': 'empty',
        'Sec-Fetch-Mode': 'cors',
        'Sec-Fetch-Site': 'same-origin',
        'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.0.0 Safari/537.36 Edg/114.0.1823.67',
        'X-Asbd-Id': '129477',
        'X-Csrftoken': 'gLlFX76z8qqwDgmh8ZIp3uFhAeX4zKdO',
        'X-Ig-App-Id': '936619743392459',
        'X-Ig-Www-Claim': 'hmac.AR0g7ECdkTdrXy37TE9AoSnMndccWbB1cqrccYOZSLfcb8sd',
        'X-Requested-With': 'XMLHttpRequest',
    } 
    r = requests.get(url,headers=headers)
    print()
    if '{"message":"","spam":true,"status":"fail"}' in r.text:
        exit('block')
    
    for i in r.json()['users']:
        gg+=1
        userL = i['username']

  
              
                
        pasw= userL
        print(f'{Y}{gg} {M}» {H}{userL} / {pasw}')
        open("combo.txt", "a").write(f'{userL}:{pasw}\n')
    if 'HI' in listoo:
        try:
            m_id=r.json()['next_max_id']
        except KeyError:
            exit()
        for i in range(9999):
            r = requests.get(f'https://i.instagram.com/api/v1/friendships/{id}/following/?count=200&max_id='+m_id,headers=headers)
            if '{"message":"","spam":true,"status":"fail"}' in r.text:
                exit('block')
            try:
                for i in r.json()['users']:
                    gg+=1
                    userL = i["username"]

  
              
                    pasw= userL


                    print(f'{Y}{gg} {M}» {H}{userL} / {pasw}')
                    open("combo.txt", "a").write(f'{userL}:{pasw}\n')
                try:
                    m_id=r.json()['next_max_id']
                except:
                    break
            except:
                if 'challenge' in r.text:
                    break
                else:
                    continue
    else:pass
    exit()	
    
rs_id = requests.get("https://i.instagram.com/api/v1/users/web_profile_info/?username=%s"%(user),headers={
    'Accept': '*/*',
    'Accept-Encoding': 'gzip, deflate, br',
    'Accept-Language': 'en-US,en;q=0.9',
    'Cookie': f'mid=Y3bGYwALAAHNwaKANMB8QCsRu7VA; ig_did=092BD3C7-0BB2-414B-9F43-3170EAED8778; ig_nrcb=1; shbid=1685054; shbts=1675191368.6684434090; rur=CLN; ig_direct_region_hint=ATN; csrftoken=gLlFX76z8qqwDgmh8ZIp3uFhAeX4zKdO; ds_user_id=921803283; sessionid={sessionid}',
    'Sec-Ch-Prefers-Color-Scheme': 'dark',
    'Sec-Ch-Ua': '"Not.A/Brand";v="8", "Chromium";v="114", "Microsoft Edge";v="114"',
    'Sec-Ch-Ua-Full-Version-List': '"Not.A/Brand";v="8.0.0.0", "Chromium";v="114.0.5735.201", "Microsoft Edge";v="114.0.1823.67"',
    'Sec-Ch-Ua-Mobile': '?0',
    'Sec-Ch-Ua-Platform': '"Windows"',
    'Sec-Ch-Ua-Platform-Version': '"15.0.0"',
    'Sec-Fetch-Dest': 'empty',
    'Sec-Fetch-Mode': 'cors',
    'Sec-Fetch-Site': 'same-origin',
    'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.0.0 Safari/537.36 Edg/114.0.1823.67',
    'X-Asbd-Id': '129477',
    'X-Csrftoken': 'gLlFX76z8qqwDgmh8ZIp3uFhAeX4zKdO',
    'X-Ig-App-Id': '936619743392459',
    'X-Ig-Www-Claim': 'hmac.AR0g7ECdkTdrXy37TE9AoSnMndccWbB1cqrccYOZSLfcb8sd',
    'X-Requested-With': 'XMLHttpRequest',
});jsn3=rs_id.json()['data']['user']
id_tr = jsn3['id']
print('')


	   
    
    
         

fg(id_tr)
