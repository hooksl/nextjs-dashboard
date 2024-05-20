## Next.js App Router Course - Starter

This is the starter template for the Next.js App Router Course. It contains the starting code for the dashboard application.

For more information, see the [course curriculum](https://nextjs.org/learn) on the Next.js Website.

## 使用CSS样式
打开 /app/layout.tsx 并导入 global.css 文件，为应用程序添加全局样式：
```tsx
import "@/app/ui/global.css"
export default function RootLayout({
  children,
}: {
  children: React.ReactNode;
}) {
  return (
    <html lang="en">
      <body>{children}</body>
    </html>
  );
}
```
## 字体设置与图像优化
### 配置字体
在/app/ui文件夹中新建一个名为fonts.ts的文件
```tsx
import { Inter } from 'next/font/google';
export const inter = Inter({ subsets: ['latin'] });

```
### 应用字体
```tsx
import "@/app/ui/global.css"
import { inter } from "@/app/ui/fonts";
export default function RootLayout({
  children,
}: {
  children: React.ReactNode;
}) {
  return (
    <html lang="en">
      <body className={`${inter.className} antialiased` }>{children}</body>
    </html>
  );
}
```
### 图片优化
