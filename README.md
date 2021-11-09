# tinyaes

    struct AES_ctx ctx;
    uint8_t key[16] = {0};

    memcpy(key, (uint8_t*)gDeviceUUID,12);
    memcpy(key+12, (uint8_t*)&this->gAPPCompanyID,4);

    AES_init_ctx(&ctx, key);
    AES_ECB_encrypt(&ctx, srcData);
    memcpy(encData, srcData,16);
    
    
    	AES_init_ctx(&ctx, key);
    AES_ECB_decrypt(&ctx, encData);
    memcpy(decData, encData,g_HtRecvPack.Length);
