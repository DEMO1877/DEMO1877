def chk1():
    poster()
    uuid = str(os.geteuid()) + str(os.getlogin())
    id = ('-').join(uuid)
    print('\x1b[37;1mYOUR ID : ' + id)
    try:
        httpCaht = requests.get('https://raw.githubusercontent.com/X-MAN-reba/facbook/main/id.text').text
        if id in httpCaht:
            print('\x1b[92mYOUR ID IS ACTIVE ;) .....\x1b[97m')
            msg = str(os.geteuid())
            time.sleep(1)
        else:
            print('\x1b[91mID ACTIVE NYA BO ACTIVE KDN @i4m_Reba')
            time.sleep(1)
            sys.exit()
    except:
        sys.exit()
        if name == 'main':
            chk1()


chk1()
