# 創造你的蒙娜麗莎！ （NFT 產生教學 電腦版）

## 前置作業

1. 用任何工具製作出你的一幅畫 ([線上繪圖](https://www.autodraw.com/)) 或是一張 jpg/png 照片
1. 安裝 [Metamask](https://metamask.io/download.html) (Chrome)

## 操作步驟

1. Metamask 連接至 **Rinkeby** 測試鏈
1. 複製自己的錢包地址
1. 拿[測試幣](https://faucet.rinkeby.io/)
    1. 發一篇 tweeter
    2. 發一篇 facebook
    > Requesting faucet funds into 0x000000000000000000000000000000000000000 on the #Rinkeby #Ethereum test network.
1. 生成 NFT Metadata (你的畫作、球卡...)
    - 產生圖片連結 
        1. [上傳圖片](https://imgur.com/upload) 
        2. 複製圖片位址 →  ex: `https://i.imgur.com/cRt8VMe.png`
    - 產生 JSON 字串
        1. 開啟 [JSON Keeper](https://jsonkeeper.com/) 
        1. 複製貼上 
        ```
        {"name":"輸入名稱","description":"輸入描述","image":"輸入圖片連結"}
        ```
    - 產生 JSON 連結 
        - ex: `https://jsonkeeper.com/b/PYNY`
1. 在 [Remix](http://remix.ethereum.org/) 上發布 [erc721.sol](./erc721.sol)、[Address.sol](,/Address.sol)
    1. 開啟 Remix
    2. 新增 Address.sol 空白檔案
    3. 複製貼上 Address.sol
    4. 新增 erc721.sol 空白檔案
    3. 複製貼上 erc721.sol
1. 在 [Remix](http://remix.ethereum.org/) mint NFT
    - compile erc721.sol
    - deploy (environment: Injected Web3 -> 下方顯示為自己的錢包地址)
    - 小狐狸確認交易
    - 出現綠色✅
    - 展開下方合約，出現許多的按鈕
    - 按鈕「mint」 → 輸入上面的 JSON 連結
    - 點擊 mint
    - 小狐狸確認交易
    - 出現綠色✅
    - 你的 NFT 就完成了！
1. 在 [opensea](https://testnets.opensea.io/account) 查看 NFT (使用 rinkeby testnet)

