# 概要
React + Vite(+tailwind)をvercel上へデプロイするまでの流れと、サンプルデータです。

#### テンプレートを使って、とりあえずデプロイしたい方

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/import/git?s=https://github.com/testkun08080/ReactVite-vercel)

#### サンプルページ
https://react-vite-vercel-ten.vercel.app/


## 事前インストール必要なもの

- npm Node.js 20+ (インストールは[こちら](https://nodejs.org/en/download/))
- Vercel CLI (インストールは[こちら](https://vercel.com/docs/cli#installing-vercel-cli/))



## ローカル上でセットアップから起動

1. **ローカルへクローンする**
    ```bash
    git clone https://github.com/testkun08080/ReactVite-vercel.git
   ```

2. **仮想環境の構築**
    ```bash
    cd ReactVite-vercel/app
    npm install
   ```
3. **ローカル起動**  
   以下コマンドを叩いて、ブラウザで<http://localhost:3000>確認できるはずです。
    ```bash
    npm run dev
   ```

## Vercel CLI を使ってテストからデプロイ
1. **ローカル起動**  
   app階層にターミナルが移動していること路確認してください。  
   あとはお好きなプロジェクト名などに適宜変えてください。  
   以下のように順調に進めば、ブラウザで<http://localhost:3000>確認できるはずです。
   
    ```bash
    vercel dev
    ```
   以下ターミナルのサンプル表示
    ```bash
    YOURUSERNAME ReactVIte-vercel % vercel dev
    Vercel CLI 42.3.0
    ? Set up and develop “~/Git/ReactVIte-vercel”? yes
    ? Which scope should contain your project? testkun08080's projects
    ? Link to existing project? no
    ? What’s your project’s name? react-vite-vercel
    ? In which directory is your code located? ./app
    Local settings detected in vercel.json:
    Auto-detected Project Settings (Vite): 
    - Build Command: vite build
   - Development Command: vite --port $PORT
   - Install Command: `yarn install`, `pnpm install`, `npm install`, or `bun install`
   - Output Directory: dist
   ? Want to modify these settings? no
   🔗  Linked to testkun08080s-projects/react-vite-vercel (created .vercel)
   > Running Dev Command “vite --port $PORT”

     VITE v6.3.5  ready in 389 ms

     ➜  Local:   http://localhost:3000/
     ➜  Network: use --host to expose
     ➜  press h + enter to show help
   > Ready! Available at http://localhost:3000
      ```

3. **vercelへデプロイ（プレビューとして）**
    ```bash
    vercel
   ```

4. **vercelへデプロイ（プロダクトとして）**
    ```bash
    vercel --prod
   ```
