# moontv-config — 自用 MoonTV 配置订阅（合并版）

个人自用的 MoonTV / MoonTVPlus / LunaTV 配置订阅。在原订阅的基础上合并了多个公开配置仓库的存活源，去重后共 **97 个源**（原有 69 + 新增 28）。

## 订阅地址

```
https://raw.githubusercontent.com/DaLongZhuaZi/moontv-config/main/sub.txt
```

文件说明：

- `sub.txt` — 订阅文件，上方地址即订阅链接（内容为 `config.json` 的 Base58 编码，MoonTV 系订阅的标准格式）
- `config.json` — 同一配置的可读 JSON（`api_site` 结构），可直接粘贴到后台配置中

## 来源与合并方法（2026-10-07）

基底是当时在用的订阅 **hafrey1/LunaTV-config** 完整版（订阅服务 `https://pz.v88.qzz.io?format=2&source=full`，GitHub 仓库 https://github.com/hafrey1/LunaTV-config ），共 69 个源，**key、名称、地址全部原样保留未动**——MoonTVPlus 的特殊源（里世界）标记按 key 关联，保留 key 才能保证切到本订阅后原有标记不丢失。

候选来源（均为 GitHub 公开仓库）：

| 仓库 | 清单规模 | 2026-10-07 测活 |
| --- | --- | --- |
| hafrey1/LunaTV-config（基底） | 69 | 54 |
| smallmain/moontv-aggr-config（full-plus18，聚合多仓） | 94 | 79 |
| vodtv/api | 77 | 51 |
| pqguanyinli/moontv_shipinyuan | 93 | 57 |
| heardic/shipinyuan | 94（标称 101，去重后 94） | 57 |

合并步骤：五份清单按 API 地址去重得到 140 个唯一源 → 逐个测活（请求 `?ac=videolist`，能返回 JSON 列表判活，共 82 活）→ 基底 69 个无论死活全部保留（测活点在海外出口，个别源可能仅从特定网络可达，不凭异地测活删自有源）→ 仅把基底之外、且实测存活的 **28 个新源**加入（其中 🔞 源 6 个）。

测活说明：测活于 2026-10-07 在代理出口完成，结果是单时点、单出口的参考；资源站域名更换频繁，本表会随时间衰减。

## 全部 97 个源及出处

| # | 名称 | key | API | 来源 |
| --- | --- | --- | --- | --- |
| 1 | 🎬-爱奇艺- | `iqiyizyapi.com` | https://iqiyizyapi.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 2 | 🎬豆瓣资源 | `dbzy.tv` | https://caiji.dbzy5.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 3 | 🎬茅台资源 | `mtzy.me` | https://caiji.maotaizy.cc/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 4 | 🎬卧龙资源 | `wolongzyw.com` | https://wolongzyw.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 5 | 🎬iKun资源 | `ikunzy.com` | https://ikunzyapi.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 6 | 🎬电影天堂 | `dyttzyapi.com` | http://caiji.dyttzyapi.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 7 | 🎬猫眼资源 | `www.maoyanzy.com` | https://api.maoyanapi.top/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 8 | 🎬量子资源 | `cj.lzcaiji.com` | https://cj.lzcaiji.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 9 | 🎬360 资源 | `360zy.com` | https://360zyzz.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 10 | 🎬极速资源 | `jszyapi.com` | https://jszyapi.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 11 | 🎬魔都资源 | `www.moduzy.net` | https://www.mdzyapi.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 12 | 🎬非凡资源 | `ffzyapi.com` | https://api.ffzyapi.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 13 | 🎬暴风资源 | `bfzy.tv` | https://bfzyapi.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 14 | 🎬最大资源 | `zuida.xyz` | https://api.zuidapi.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 15 | 🎬无尽资源 | `wujinzy.me` | https://api.wujinapi.me/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 16 | 🎬新浪资源 | `xinlangapi.com` | https://api.xinlangapi.com/xinlangapi.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 17 | 🎬旺旺资源 | `api.wwzy.tv` | https://api.wwzy.tv/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 18 | 🎬速播资源 | `www.subozy.com` | https://subocaiji.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 19 | 🎬金鹰点播 | `jinyingzy.com` | https://jyzyapi.com/provide/vod/from/jinyingyun/at/json | 原有 · hafrey1/LunaTV-config |
| 20 | 🎬飘零资源 | `p2100.net` | https://p2100.net/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 21 | 🎬U酷影视 | `api.ukuapi88.com` | https://api.ukuapi88.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 22 | 🎬光速资源 | `api.guangsuapi.com` | https://api.guangsuapi.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 23 | 🎬红牛资源 | `www.hongniuzy.com` | https://www.hongniuzy2.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 24 | 🎬魔都动漫 | `caiji.moduapi.cc` | https://caiji.moduapi.cc/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 25 | 🎬如意资源 | `www.ryzyw.com` | https://cj.rycjapi.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 26 | 🎬豪华资源 | `www.haohuazy.com` | https://hhzyapi.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 27 | 🎬百度云zy | `bdzy1.com` | https://pz.v88.qzz.io/?url=https://api.apibdzy.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 28 | 🎬艾旦影视 | `lovedan.net` | https://pz.v88.qzz.io/?url=https://lovedan.net/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 29 | 🎬量子影视 | `lzizy.net` | https://cj.lziapi.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 30 | 🎬最大点播 | `zuidazy.co` | https://zuidazy.me/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 31 | 🎬无尽影视 | `wujinzy.com` | https://api.wujinapi.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 32 | 🎬旺旺短剧 | `wwzy.tv` | https://wwzy.tv/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 33 | 🎬优质资源 | `1080zyk4.com` | https://api.yzzy-api.com/inc/apijson.php | 原有 · hafrey1/LunaTV-config |
| 34 | 🎬虎牙资源 | `www.huyaapi.com` | https://www.huyaapi.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 35 | 🎬鸭鸭资源 | `yayazy3.com` | https://cj.yayazy.net/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 36 | 🎬索尼资源 | `suonizy.net` | https://suoniapi.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 37 | 🎬快车资源 | `kuaichezy.com` | https://caiji.kuaichezy.org/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 38 | 🎬闪电资源 | `shandianzy.com` | https://xsd.sdzyapi.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 39 | 🎬樱花资源 | `yhzy.cc` | https://m3u8.apiyhzy.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 40 | 🔞麻豆视频 | `91md.me` | https://91md.me/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 41 | 🔞155-资源 | `155zy2.com` | https://155api.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 42 | 🔞玉兔资源 | `apiyutu.com` | https://apiyutu.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 43 | 🔞番号资源 | `fhapi9.com` | http://fhapi9.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 44 | 🔞-老色逼- | `apilsbzy1.com` | https://apilsbzy1.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 45 | 🔞小鸡资源 | `xiaojizy.live` | https://api.xiaojizy.live/provide/vod | 原有 · hafrey1/LunaTV-config |
| 46 | 🔞黄色仓库 | `hsckzy.xyz` | https://hsckzy.xyz/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 47 | 🔞-大奶子- | `apidanaizi.com` | https://apidanaizi.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 48 | 🔞jkun资源 | `jkunzyapi.com` | https://jkunzyapi.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 49 | 🔞乐播资源 | `lbapi9.com` | https://lbapi9.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 50 | 🔞奶香资源 | `Naixxzy.com` | https://Naixxzy.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 51 | 🔞森林资源 | `slapibf.com` | https://beiyong.slapibf.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 52 | 🔞辣椒资源 | `apilj.com` | https://apilj.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 53 | 🔞鲨鱼资源 | `shayuapi.com` | https://shayuapi.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 54 | 🔞豆豆资源 | `doudouzy.com` | https://api.douapi.cc/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 55 | 🔞滴滴资源 | `didizy.com` | https://api.ddapi.cc/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 56 | 🔞黑料资源 | `heiliaozy.cc` | https://www.heiliaozyapi.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 57 | 🔞桃花资源 | `thzy8.me` | https://thzy1.me/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 58 | 🔞精品资源 | `www.jingpinx.com` | https://www.jingpinx.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 59 | 🔞 CK-资源 | `ckzy.me` | https://ckzy.me/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 60 | 🔞souavZY | `souavzyw.com` | https://api.souavzyw.net/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 61 | 🔞细胞资源 | `www.xxibaozyw.com` | https://www.xxibaozyw.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 62 | 🔞香蕉资源 | `xiangjiaozyw.com` | https://www.xiangjiaozyw.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 63 | 🔞-美少女- | `www.msnii.com` | https://www.msnii.com/api/json.php | 原有 · hafrey1/LunaTV-config |
| 64 | 🔞-黄AVZY | `www.pgxdy.com` | https://www.pgxdy.com/api/json.php | 原有 · hafrey1/LunaTV-config |
| 65 | 🔞白嫖资源 | `www.kxgav.com` | https://www.kxgav.com/api/json.php | 原有 · hafrey1/LunaTV-config |
| 66 | 🔞杏吧资源 | `xingba111.com` | https://xingba222.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 67 | 🔞大地资源 | `dadizy11.com` | https://dadiapi.com/feifei | 原有 · hafrey1/LunaTV-config |
| 68 | 🔞色猫资源 | `semaozy1.com` | https://caiji.semaozy.net/inc/apijson_vod.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 69 | 🔞-奥斯卡- | `aosikazy.com` | https://aosikazy.com/api.php/provide/vod | 原有 · hafrey1/LunaTV-config |
| 70 | 🎬金鹰点播 | `jinyingzy_com` | https://jinyingzy.com/api.php/provide/vod | 新增 · smallmain/moontv-aggr-config / vodtv/api / pqguanyinli/moontv_shipinyuan / heardic/shipinyuan |
| 71 | 🎬360资源 | `360zy_com` | https://360zy.com/api.php/provide/vod | 新增 · smallmain/moontv-aggr-config / pqguanyinli/moontv_shipinyuan / heardic/shipinyuan |
| 72 | 🎬天涯资源 | `tyyszy_com` | https://tyyszy.com/api.php/provide/vod | 新增 · smallmain/moontv-aggr-config / pqguanyinli/moontv_shipinyuan / heardic/shipinyuan |
| 73 | 🎬百度云zy | `api_apibdzy_com` | https://api.apibdzy.com/api.php/provide/vod | 新增 · smallmain/moontv-aggr-config / pqguanyinli/moontv_shipinyuan / heardic/shipinyuan |
| 74 | 🎬1080资源库 | `api_1080zyku_com` | https://api.1080zyku.com/inc/api_mac10.php | 新增 · smallmain/moontv-aggr-config / pqguanyinli/moontv_shipinyuan / heardic/shipinyuan |
| 75 | 🎬wujinapi无尽 | `api_wujinapi_cc` | https://api.wujinapi.cc/api.php/provide/vod | 新增 · smallmain/moontv-aggr-config / pqguanyinli/moontv_shipinyuan / heardic/shipinyuan |
| 76 | 🎬无尽资源3 | `api_wujinapi_net` | https://api.wujinapi.net/api.php/provide/vod | 新增 · smallmain/moontv-aggr-config / pqguanyinli/moontv_shipinyuan / heardic/shipinyuan |
| 77 | 🎬牛牛点播 | `api_niuniuzy_me` | https://api.niuniuzy.me/api.php/provide/vod | 新增 · smallmain/moontv-aggr-config / pqguanyinli/moontv_shipinyuan / heardic/shipinyuan |
| 78 | 🎬神马云 | `api_1080zyku_com_2` | https://api.1080zyku.com/inc/apijson.php | 新增 · smallmain/moontv-aggr-config / pqguanyinli/moontv_shipinyuan / heardic/shipinyuan |
| 79 | 🎬艾旦影视 | `lovedan_net` | https://lovedan.net/api.php/provide/vod | 新增 · smallmain/moontv-aggr-config |
| 80 | 🎬金鹰资源 | `jyzyapi_com` | https://jyzyapi.com/api.php/provide/vod | 新增 · smallmain/moontv-aggr-config / pqguanyinli/moontv_shipinyuan / heardic/shipinyuan |
| 81 | 🎬金鹰资源采集网 | `jyzyapi_com_2` | https://jyzyapi.com/provide/vod | 新增 · smallmain/moontv-aggr-config / pqguanyinli/moontv_shipinyuan / heardic/shipinyuan |
| 82 | 🎬闪电资源 | `sdzyapi_com` | https://sdzyapi.com/api.php/provide/vod | 新增 · smallmain/moontv-aggr-config / pqguanyinli/moontv_shipinyuan / heardic/shipinyuan |
| 83 | 🎬非凡资源 | `cj_ffzyapi_com` | https://cj.ffzyapi.com/api.php/provide/vod | 新增 · smallmain/moontv-aggr-config / pqguanyinli/moontv_shipinyuan / heardic/shipinyuan |
| 84 | 🎬IK | `ikunzyapi_com` | https://ikunzyapi.com/api.php/provide/vod/from/ikm3u8 | 新增 · smallmain/moontv-aggr-config |
| 85 | 🎬天涯影视 | `tyyszyapi_com` | https://tyyszyapi.com/api.php/provide/vod | 新增 · smallmain/moontv-aggr-config |
| 86 | 🎬无广1线 (非凡) | `yonghu_ffzyapi8_com` | https://yonghu.ffzyapi8.com/api.php/provide/vod/from/ffm3u8/at/json | 新增 · smallmain/moontv-aggr-config |
| 87 | 🎬速播资源 | `subocj_com` | https://subocj.com/api.php/provide/vod | 新增 · smallmain/moontv-aggr-config |
| 88 | 🎬非凡资源站 | `ffzy5_tv` | https://ffzy5.tv/api.php/provide/vod | 新增 · smallmain/moontv-aggr-config |
| 89 | 🎬黄色资源啊啊 | `hsckzy888_com` | https://hsckzy888.com/api.php/provide/vod | 新增 · smallmain/moontv-aggr-config / pqguanyinli/moontv_shipinyuan / heardic/shipinyuan |
| 90 | 🎬🔅樱花资源ᴴ | `yhzy_cc` | https://yhzy.cc/api.php/provide/vod | 新增 · smallmain/moontv-aggr-config |
| 91 | 🔞souav资源 | `api_souavzy_vip` | https://api.souavzy.vip/api.php/provide/vod | 新增 · smallmain/moontv-aggr-config / pqguanyinli/moontv_shipinyuan / heardic/shipinyuan |
| 92 | 🔞杏吧资源 | `xingba111_com` | https://xingba111.com/api.php/provide/vod | 新增 · smallmain/moontv-aggr-config / pqguanyinli/moontv_shipinyuan / heardic/shipinyuan |
| 93 | 🔞森林资源 | `slapibf_com` | https://slapibf.com/api.php/provide/vod | 新增 · smallmain/moontv-aggr-config / pqguanyinli/moontv_shipinyuan / heardic/shipinyuan |
| 94 | 🔞淫水机资源 | `www_xrbsp_com` | https://www.xrbsp.com/api/json.php | 新增 · smallmain/moontv-aggr-config / pqguanyinli/moontv_shipinyuan / heardic/shipinyuan |
| 95 | 🔞豪华资源 | `hhzyapi_com` | https://hhzyapi.com/api.php/provide/vod/from/hhm3u8/at/json | 新增 · smallmain/moontv-aggr-config |
| 96 | 🔞香奶儿资源 | `www_gdlsp_com` | https://www.gdlsp.com/api/json.php | 新增 · smallmain/moontv-aggr-config / pqguanyinli/moontv_shipinyuan / heardic/shipinyuan |
| 97 | TV-步步高资源 | `api_yparse_com` | https://api.yparse.com/api/json | 新增 · pqguanyinli/moontv_shipinyuan / heardic/shipinyuan |

## 备注

- 本仓库为公开仓库：MoonTV 的配置订阅需要被服务端免登录拉取，订阅文件本质如此（与基底订阅相同）。文件内只有公开的资源站接口地址，不含任何账号、密钥。
- 原订阅（pz.v88.qzz.io）未做任何改动，仍可随时切回。
