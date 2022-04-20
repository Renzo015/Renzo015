62
63
64
65
66
67
68
69
70
71
72
73
74
75
76
77
78
79
80
81
82
83
84
85
86
87
88
89
90
91
92
93
▼
▼
▼
▼
▼
##    MIT License   ## Repo: github.com/cliphd/TTNC
                "x-ladon": "66i4D/A/9Duggct+t+TzgyNDPCpWofgabGLDBhqo5JcUg25R",
                "x-gorgon": "0404c0d24005a6dd2c0f90f095989f1cbbe822c080373f154aef",
                "x-khronos": "1637702083",
                "x-argus": "akF3zOzHe0jW4MD20rF9/IpQbtX2kWt7VmI17WF+n62ONJb7BvQO2kCiNlNutTEUeyxbpKFvQeKNZJfAODyxTM0vbS/9e9NWLaxmJNdsEr0ZOua7B2fZyxOetObzPkkkg1sL+DOi2Y5RsRTXNxhvRp3ndhSfmMHxN83rSR7/0pKIsabl/cLFXcV6r78ctYqOCLiSGFip0exaU1rP5re0ROKiSPauZGs7t2sJQXzyn8hfmKQywiGxdTZqKSZdecHYdmgbWBqHb99hzlqzusJdcRih73y+pRtse/j5IYpYa7hIjVjewRMbgwx7yHQ1hXXeibrjTW7m4XhzX38Gw0Ua8i99p2Fz9Y9WIzpCm591cBoOuQ==",
                "host": "api22-normal-c-useast1a.tiktokv.com",
                "connection": "Keep-Alive"
            }
            r = requests.post("https://api22-normal-c-useast1a.tiktokv.com/passport/login_name/check/?passport-sdk-version=19&iid=7037880313762858758&device_id=6906478625937278469&ac=wifi&channel=googleplay&aid=1233&app_name=musical_ly&version_code=220105&version_name=22.1.5&device_platform=android&ab_version=22.1.5&ssmix=a&device_type=G011A&device_brand=google&language=en&os_api=25&os_version=7.1.2&openudid=c0575264c704f9c6&manifest_version_code=2022201050&resolution=1280*720&dpi=240&update_version_code=2022201050&_rticket=1638647824321&current_region=US&app_type=normal&sys_region=US&mcc_mnc=31610&timezone_name=AsiaShanghai&reSSIDence=US&ts=1638647824&timezone_offset=28800&build_number=22.1.5&region=US&uoo=0&app_language=en&carrier_region=US&locale=en&op_region=US&ac2=wifi&cdid=6ad560a8-8209-4fe3-b771-6bbe64880e4c&support_webview=1&okhttp_version=4.0.69.4-tiktok", headers=headers, params={"login_name":username})
            if "success" in r.text:
                print(f"{Fore.GREEN}[{Fore.RESET}AVALIBLE{Fore.GREEN}]{Fore.RESET} {username}")
                Send(username)
            else:
                print(f"{Fore.RED}[{Fore.RESET}ERROR{Fore.RED}]{Fore.RESET} Banned username.")
        elif r.status_code == 200 or 204:
            print(f"{Fore.RED}[{Fore.RESET}TAKEN{Fore.RED}]{Fore.RESET} {username}")
  
banner = f"""
                   {Fore.GREEN}╔╦╗╔╦╗{Fore.MAGENTA}╔╗╔╔═╗
                    {Fore.GREEN}║  ║ {Fore.MAGENTA}║║║║  
                    {Fore.GREEN}╩  ╩ {Fore.MAGENTA}╝╚╝╚═╝ {Fore.RESET}
                TikTok: cliphd1
                github.com/cliphd/TTNC
"""
print(banner)
Webhook = input(f'             {Fore.MAGENTA}Discord WebhookURL{Fore.RESET}:\n ')

if __name__ == "__main__":
    time.sleep(1)
    os.system('cls||clear')
    print(banner)
    for i in range(10):
        threading.Thread(target=Check()).start
