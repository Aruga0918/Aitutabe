<template>
    <b-container class="commlist" >
    <div class="d-flex" style="align-items: center; justify-content: center; border-top-style: ridge; border-bottom-style: groove; height: 150px;" v-for="shop in shops" :key="shop.name">
    <div class="d-flex" style="align-items: center; width: 70%;">
        <img :src="shop.img" class="d-inline-block" style="height: 100px; width: 100px; float:left">
            <div class="d-inline-block ml-auto mr-auto" style="width:260px">
                <p class="d-inline ml-auto">{{shop.name}}</p>
                <p style="font-size: 6px;">{{shop.opentime}}</p>
                <!-- <p style="color: gray; margin-bottom: 4px;">-場所- {{shop.address}}</p>
                 -->
            </div>
        
    </div> 
    </div>
    </b-container>
</template>

<script src="https://www.promisejs.org/polyfills/promise-7.0.4.min.js"></script>
<script>

export default{
   
   data(){
       return{
       shops: [
           {
    "name": "にぎりの徳兵衛 仙台駅前店",
    "category": "和食",
    "img": "https://imgfp.hotp.jp/IMGH/10/90/P027711090/P027711090_100.jpg",
    "opentime": "月～日、祝日、祝前日: 11:00～22:15 （料理L.O. 22:00 ドリンクL.O. 22:00）",
    "address": "宮城県仙台市青葉区中央３-1-24　荘銀ビル2F",
    "lat": 38.260470197,
    "lng": 140.8789994015,
    "budget": "昼：1200円　夜：1600円",
    "id": "J001039291",
    "menu": {
        "国産本まぐろ赤身": "418円（税込）",
        "穴子天": "418円（税込）",
        "穴子一本焼き": "418円（税込）",
        "120円(税込132円)": "132円（税込）",
        "180円（税込198円）": "198円（税込）",
        "220円（税込242円）": "242円（税込）",
        "260円（税込286円）": "286円（税込）",
        "300円（税込330円）": "330円（税込）",
        "はまちネギ塩炙り": "286円（税込）",
        "サーモンネギ塩炙り": "286円（税込）",
        "びんちょうマヨネーズ炙り": "286円（税込）",
        "サーモンタルタル炙り": "286円（税込）",
        "えびガーリック炙り": "286円（税込）",
        "えんがわ漬け炙り": "330円（税込）",
        "赤えびマヨネーズ炙り": "330円（税込）",
        "炙り鯖の押し寿司": "418円（税込）",
        "国産本まぐろとろ炙り": "638円（税込）",
        "うなぎ": "418円（税込）",
        "鯖の押し寿司": "418円（税込）",
        "いくら": "418円（税込）",
        "かんぱち": "418円（税込）",
        "国産本まぐろ中とろ": "528円（税込）",
        "とろ鉄火巻き": "528円（税込）",
        "数の子": "528円（税込）",
        "本ずわい蟹": "528円（税込）",
        "生うに": "638円（税込）",
        "貝三昧": "418円（税込）",
        "まぐろ三昧": "528円（税込）",
        "サラダ三昧": "198円（税込）",
        "彩り三昧": "330円（税込）",
        "光物三昧": "330円（税込）",
        "えび三昧": "418円（税込）",
        "炙り三昧": "418円（税込）",
        "刺身三点盛り": "814円（税込）",
        "貝刺し三点盛り": "858円（税込）",
        "お子様プレート": "528円（税込）",
        "お子様手巻き寿司セット": "528円（税込）",
        "お子様寿司セット": "528円（税込）",
        "お子様うどん": "286円（税込）",
        "だし巻き玉子": "330円（税込）",
        "だし巻き玉子大根おろし添え": "374円（税込）",
        "めんたい・大葉入りだし巻き玉子": "374円（税込）",
        "ネギ入りだし巻き玉子": "374円（税込）",
        "天ぷら盛り合せ": "748円（税込）",
        "山盛りポテト": "242円（税込）",
        "げその唐揚げ": "286円（税込）",
        "れんこん海鮮はさみ揚げ": "286円（税込）",
        "鶏の唐揚げ": "418円（税込）",
        "かに甲羅焼き": "528円（税込）",
        "本日のカマ焼き": "748円（税込）",
        "枝豆": "198円（税込）",
        "なす漬け一本": "418円（税込）",
        "海鮮サラダ（ミニ）": "330円（税込）",
        "あさり汁/のり汁": "198円（税込）",
        "うどん各種": "330円（税込）",
        "えび天うどん": "528円（税込）",
        "あら汁": "242円（税込）",
        "茶碗蒸し": "286円（税込）"
    }
},
{
    "name": "大戸屋 仙台ロフト店",
    "category": "和食",
    "img": "https://imgfp.hotp.jp/IMGH/53/95/P036735395/P036735395_100.jpg",
    "opentime": "月～日、祝日、祝前日: 11:00～20:00 （料理L.O. 19:30 ドリンクL.O. 19:30）",
    "address": "宮城県仙台市青葉区中央１－１０－１０仙台ロフト８Ｆ",
    "lat": 38.260132227,
    "lng": 140.880588724,
    "budget": "1500円",
    "id": "J000301784",
    "menu": {
        "食べきれないお料理の「お持ち帰り」について": "-",
        "選べるご飯【白米から五穀米に変更できます】": "-",
        "大戸屋ランチ": "740円（税込）",
        "大戸屋ミックス": "1,080円（税込）",
        "チキンかあさん煮": "890円（税込）",
        "炭火焼きチキンの葱ソース": "790円（税込）",
        "梅おろしチキンカツ": "790円（税込）",
        "大戸屋風チキン南蛮": "860円（税込）",
        "香味唐揚げ": "790円（税込）",
        "豆味噌デミグラスソースのハンバーグ": "940円（税込）",
        "黒酢ポン酢の和風おろしハンバーグ": "890円（税込）",
        "鶏と野菜の黒酢あん": "890円（税込）",
        "すけそう鱈と野菜の黒酢あん": "920円（税込）",
        "おおとや三元豚と野菜の黒酢あん": "950円（税込）",
        "豚と野菜の塩麹炒め": "790円（税込）",
        "豚と野菜の豆鼓味噌炒め": "840円（税込）",
        "豚の生姜焼き": "790円（税込）",
        "おおとや三元豚のロースかつ": "980円（税込）",
        "プルコギ牛肉炒め": "980円（税込）",
        "さばの炭火焼き": "840円（税込）",
        "さばの竜田揚げ香味ねぎソース": "890円（税込）",
        "しまほっけの炭火焼き": "980円（税込）",
        "さばの味噌煮": "890円（税込）",
        "沖目鯛の醤油麹漬け炭火焼き": "980円（税込）",
        "牛プルコギの彩りサラダボウル": "940円（税込）",
        "バジルチキンの彩りサラダボウル": "890円（税込）",
        "ばくだん丼": "840円（税込）",
        "【まぐろ増量】ばくだん丼": "990円（税込）",
        "かあさんの玉子とじ": "940円（税込）",
        "チキン味噌かつ煮": "890円（税込）",
        "豆腐と鶏肉のトロトロ煮": "940円（税込）",
        "辛旨 豚キムチ鍋": "980円（税込）",
        "［サラダ］グリーンサラダ": "240円（税込）",
        "［サラダ］ひんやり豆腐サラダ": "290円（税込）",
        "［サラダ］千切りキャベツサラダ": "190円（税込）",
        "［小鉢］お豆腐ねばねば小鉢": "290円（税込）",
        "［小鉢］大戸屋風ばくだん小鉢": "290円（税込）",
        "［小鉢］ひんやり豆腐": "190円（税込）",
        "［小鉢］アカモク小鉢": "190円（税込）",
        "［サラダ］ポテトサラダ": "190円（税込）",
        "［小鉢］ひじきの煮物": "190円（税込）",
        "［小鉢］金平ごぼう": "190円（税込）",
        "［小鉢］ほうれん草の胡麻和え": "190円（税込）",
        "［おかず］ミニ野菜の黒酢あん": "290円（税込）",
        "［おかず］ミニ鶏の黒酢あん": "350円（税込）",
        "［おかず］ミニすけそう鱈の黒酢あん": "350円（税込）",
        "［おかず］ミニ豚の黒酢あん": "380円（税込）",
        "［おかず］かぼちゃコロッケ": "200円（税込）",
        "［おかず］ミニ香味唐揚げ": "200円（税込）",
        "［おかず］ミニさばの炭火焼き": "350円（税込）",
        "［おかず］ミニほっけの炭火焼き": "380円（税込）",
        "[ご飯]削りたて鰹本枯節のおかかごはんセット": "90円（税込）",
        "［ご飯のお供］きみだま": "80円（税込）",
        "［ご飯のお供］納豆": "90円（税込）",
        "［ご飯のお供］生たまご": "50円（税込）",
        "［ご飯のお供］とろろ": "110円（税込）",
        "[ご飯]削りたて鰹本枯節": "50円（税込）",
        "［ご飯］五穀ご飯(180g)": "190円（税込）",
        "［ご飯］ご飯(180g)": "190円（税込）",
        "［味噌汁］たっぷり野菜の麦みそ汁": "250円（税込）",
        "［味噌汁］": "70円（税込）",
        "お子様オムライスプレート": "390円（税込）",
        "お子様野菜カレー": "390円（税込）",
        "お子様うどんと唐揚げ": "390円（税込）",
        "大戸屋ティラミス　黒蜜きな粉": "290円（税込）",
        "たまごプリン": "290円（税込）",
        "もちもちコーヒーゼリー": "290円（税込）",
        "ミルクアイスクリーム": "190円（税込）",
        "抹茶アイスクリーム": "190円（税込）"
    }
},
{
    "name": "海鮮三崎港 仙台クリスロード",
    "category": "和食",
    "img": "https://imgfp.hotp.jp/IMGH/61/05/P036876105/P036876105_100.jpg",
    "opentime": "月～日、祝日、祝前日: 11:00～21:00",
    "address": "宮城県仙台市青葉区中央２丁目５番７号",
    "lat": 38.2615422205,
    "lng": 140.8764381843,
    "budget": "1500円～2500円",
    "id": "J001260857",
    "menu": {}
},
{
    "name": "伊達の牛たん本舗 本店",
    "category": "和食",
    "img": "https://imgfp.hotp.jp/IMGH/38/87/P016593887/P016593887_100.jpg",
    "opentime": "月～日、祝日、祝前日: 11:00～20:00 （料理L.O. 19:30 ドリンクL.O. 19:30）",
    "address": "宮城県仙台市青葉区中央４-１０-１１",
    "lat": 38.2570059418,
    "lng": 140.8812804776,
    "budget": "1,500円（通常平均）　1,500円（ランチ平均）",
    "id": "J000101109",
    "menu": {
        "芯たん定食 《数量限定メニュー》": "2,300円",
        "芯たん焼き　単品 《数量限定》": "1,910円",
        "牛たん定食　-塩味、みそ味、ミックス-": "1人前1,820円",
        "牛たん焼き　単品": "1人前1,430円",
        "牛たんシチュー定食": "1,540円",
        "牛たんカレー": "1,100円"
    }
},
{
    "name": "丸亀製麺 仙台東口店",
    "category": "和食",
    "img": "https://imgfp.hotp.jp/IMGH/79/30/P024347930/P024347930_100.jpg",
    "opentime": "月～日、祝日、祝前日: 11:00～21:00 （料理L.O. 20:30 ドリンクL.O. 20:30）",
    "address": "宮城県仙台市宮城野区榴岡２－１－２５仙台BIVI1F",
    "lat": 38.2610719311,
    "lng": 140.8836850781,
    "budget": "500円（通常）",
    "id": "J000842064",
    "menu": {
        "釜揚げうどん(温)": "並：290円",
        "釜玉うどん(温)": "並：350円",
        "明太釜玉うどん(温)": "並：410円",
        "釜揚げ家族うどん": "1260円",
        "とろろ醤油うどん(温・冷)": "並：350円",
        "ぶっかけうどん(温・冷)": "並：290円",
        "とろ玉うどん(温・冷)": "並：410円",
        "おろし醤油うどん(温・冷)": "並：350円",
        "カレーうどん(温)": "並：410円",
        "かけうどん(温)": "並：290円",
        "ざるうどん(冷)": "並：290円",
        "野菜かき揚げ": "1ヶ130円",
        "かしわ天": "1ヶ130円",
        "かぼちゃ天": "1ヶ100円",
        "えび天": "1ヶ150円",
        "いか天": "1ヶ110円",
        "さつまいも天": "1ヶ100円",
        "なす天": "1ヶ110円",
        "ちくわ天": "1ヶ110円",
        "半熟玉子天": "1ヶ110円",
        "いなり": "1ヶ100円",
        "鮭": "1ヶ130円",
        "梅": "1ヶ130円",
        "明太子": "60円",
        "こんぶ": "1ヶ130円",
        "天丼用ごはん": "130円",
        "大根おろし": "60円",
        "きつねあげ": "130円",
        "とろろ": "70円",
        "温泉たまご": "60円"
    }
},
{
    "name": "伊達の牛たん本舗 牛たん通り店",
    "category": "和食",
    "img": "https://imgfp.hotp.jp/IMGH/52/23/P016685223/P016685223_100.jpg",
    "opentime": "月: 08:00～22:30 （料理L.O. 22:00 ドリンクL.O. 22:00）火～日、祝日、祝前日: 08:00～22:00 （料理L.O. 22:00 ドリンクL.O. 22:00）",
    "address": "宮城県仙台市青葉区中央１-1-1仙台駅3階",
    "lat": 38.260288924,
    "lng": 140.8822469063,
    "budget": "1,500円（通常平均）　1,500円（ランチ平均）",
    "id": "J000302316",
    "menu": {
        "芯たん定食 《数量限定メニュー》": "2,300円",
        "芯たん焼き　単品 《数量限定》": "1,910円",
        "牛たん定食　-塩味、みそ味、ミックス-": "1,820円",
        "牛たん焼き　単品": "1,430円",
        "牛たんシチュー定食": "1,540円",
        "牛たんカレー": "1,100円",
        "牛たん入りつくね": "660円",
        "牛たん肉味噌豆腐": "440円",
        "笹かまぼこ": "330円",
        "三角揚げの炭火焼き": "440円",
        "野菜サラダ": "550円",
        "とろろ": "160円",
        "テールスープ": "390円"
    }
},
{
    "name": "伊達の牛たん本舗 tekuteせんだい店",
    "category": "和食",
    "img": "https://imgfp.hotp.jp/IMGH/64/95/P016696495/P016696495_100.jpg",
    "opentime": "月～日、祝日、祝前日: 09:00～22:00 （料理L.O. 21:30 ドリンクL.O. 21:30）",
    "address": "宮城県仙台市青葉区中央１-1-1 エスパル1階",
    "lat": 38.2592237666,
    "lng": 140.8821533533,
    "budget": "1,700円（通常平均）　1,500円（ランチ平均）",
    "id": "J000797018",
    "menu": {
        "芯たん定食 《数量限定メニュー》": "2,300円",
        "芯たん焼き　単品 《数量限定》": "1,910円",
        "牛たん定食　-塩味、みそ味、ミックス-": "1,820円",
        "牛たん焼き　単品": "1,430円",
        "通定食 <薄切り>　《数量限定メニュー》": "980円",
        "牛たんシチュー定食": "1,540円",
        "牛たんカレー": "1,100円",
        "牛たん入りつくね": "660円",
        "牛たんソーセージ": "600円",
        "野菜サラダ": "550円",
        "笹かまぼこ": "330円",
        "とろろ": "160円",
        "テールスープ": "390円"
    }
},
{
    "name": "大戸屋 仙台エスパル店",
    "category": "和食",
    "img": "https://imgfp.hotp.jp/IMGH/53/95/P036735395/P036735395_100.jpg",
    "opentime": "月～日、祝日、祝前日: 11:00～22:00 （料理L.O. 21:30 ドリンクL.O. 21:30）",
    "address": "宮城県仙台市青葉区中央１-１-１仙台エスパルB１F",
    "lat": 38.2592218189,
    "lng": 140.8820341971,
    "budget": "",
    "id": "J000991210",
    "menu": {
        "食べきれないお料理の「お持ち帰り」について": "-",
        "選べるご飯【白米から五穀米に変更できます】": "-",
        "大戸屋ランチ": "740円（税込）",
        "大戸屋ミックス": "1,080円（税込）",
        "チキンかあさん煮": "890円（税込）",
        "炭火焼きチキンの葱ソース": "790円（税込）",
        "梅おろしチキンカツ": "790円（税込）",
        "大戸屋風チキン南蛮": "860円（税込）",
        "香味唐揚げ": "790円（税込）",
        "豆味噌デミグラスソースのハンバーグ": "940円（税込）",
        "黒酢ポン酢の和風おろしハンバーグ": "890円（税込）",
        "鶏と野菜の黒酢あん": "890円（税込）",
        "すけそう鱈と野菜の黒酢あん": "920円（税込）",
        "おおとや三元豚と野菜の黒酢あん": "950円（税込）",
        "豚と野菜の塩麹炒め": "790円（税込）",
        "豚と野菜の豆鼓味噌炒め": "840円（税込）",
        "豚の生姜焼き": "790円（税込）",
        "おおとや三元豚のロースかつ": "980円（税込）",
        "プルコギ牛肉炒め": "980円（税込）",
        "さばの炭火焼き": "840円（税込）",
        "さばの竜田揚げ香味ねぎソース": "890円（税込）",
        "しまほっけの炭火焼き": "980円（税込）",
        "さばの味噌煮": "890円（税込）",
        "沖目鯛の醤油麹漬け炭火焼き": "980円（税込）",
        "牛プルコギの彩りサラダボウル": "940円（税込）",
        "バジルチキンの彩りサラダボウル": "890円（税込）",
        "ばくだん丼": "840円（税込）",
        "【まぐろ増量】ばくだん丼": "990円（税込）",
        "かあさんの玉子とじ": "940円（税込）",
        "チキン味噌かつ煮": "890円（税込）",
        "豆腐と鶏肉のトロトロ煮": "940円（税込）",
        "辛旨 豚キムチ鍋": "980円（税込）",
        "［サラダ］グリーンサラダ": "240円（税込）",
        "［サラダ］ひんやり豆腐サラダ": "290円（税込）",
        "［サラダ］千切りキャベツサラダ": "190円（税込）",
        "［小鉢］お豆腐ねばねば小鉢": "290円（税込）",
        "［小鉢］大戸屋風ばくだん小鉢": "290円（税込）",
        "［小鉢］ひんやり豆腐": "190円（税込）",
        "［小鉢］アカモク小鉢": "190円（税込）",
        "［サラダ］ポテトサラダ": "190円（税込）",
        "［小鉢］ひじきの煮物": "190円（税込）",
        "［小鉢］金平ごぼう": "190円（税込）",
        "［小鉢］ほうれん草の胡麻和え": "190円（税込）",
        "［おかず］ミニ野菜の黒酢あん": "290円（税込）",
        "［おかず］ミニ鶏の黒酢あん": "350円（税込）",
        "［おかず］ミニすけそう鱈の黒酢あん": "350円（税込）",
        "［おかず］ミニ豚の黒酢あん": "380円（税込）",
        "［おかず］かぼちゃコロッケ": "200円（税込）",
        "［おかず］ミニ香味唐揚げ": "200円（税込）",
        "［おかず］ミニさばの炭火焼き": "350円（税込）",
        "［おかず］ミニほっけの炭火焼き": "380円（税込）",
        "[ご飯]削りたて鰹本枯節のおかかごはんセット": "90円（税込）",
        "［ご飯のお供］きみだま": "80円（税込）",
        "［ご飯のお供］納豆": "90円（税込）",
        "［ご飯のお供］生たまご": "50円（税込）",
        "［ご飯のお供］とろろ": "110円（税込）",
        "[ご飯]削りたて鰹本枯節": "50円（税込）",
        "［ご飯］五穀ご飯(180g)": "190円（税込）",
        "［ご飯］ご飯(180g)": "190円（税込）",
        "［味噌汁］たっぷり野菜の麦みそ汁": "250円（税込）",
        "［味噌汁］": "70円（税込）",
        "お子様オムライスプレート": "390円（税込）",
        "お子様野菜カレー": "390円（税込）",
        "お子様うどんと唐揚げ": "390円（税込）",
        "大戸屋ティラミス　黒蜜きな粉": "290円（税込）",
        "たまごプリン": "290円（税込）",
        "もちもちコーヒーゼリー": "290円（税込）",
        "ミルクアイスクリーム": "190円（税込）",
        "抹茶アイスクリーム": "190円（税込）"
    }
},
{
    "name": "大戸屋 仙台MTビル店",
    "category": "和食",
    "img": "https://imgfp.hotp.jp/IMGH/53/95/P036735395/P036735395_100.jpg",
    "opentime": "月～日、祝日、祝前日: 10:30～22:00 （料理L.O. 21:30 ドリンクL.O. 21:30）",
    "address": "宮城県仙台市宮城野区榴岡４－２－３仙台ＭＴビル１Ｆ",
    "lat": 38.2590845112,
    "lng": 140.888075902,
    "budget": "",
    "id": "J001039086",
    "menu": {
        "食べきれないお料理の「お持ち帰り」について": "-",
        "選べるご飯【白米から五穀米に変更できます】": "-",
        "大戸屋ランチ": "740円（税込）",
        "大戸屋ミックス": "1,080円（税込）",
        "チキンかあさん煮": "890円（税込）",
        "炭火焼きチキンの葱ソース": "790円（税込）",
        "梅おろしチキンカツ": "790円（税込）",
        "大戸屋風チキン南蛮": "860円（税込）",
        "香味唐揚げ": "790円（税込）",
        "豆味噌デミグラスソースのハンバーグ": "940円（税込）",
        "黒酢ポン酢の和風おろしハンバーグ": "890円（税込）",
        "鶏と野菜の黒酢あん": "890円（税込）",
        "すけそう鱈と野菜の黒酢あん": "920円（税込）",
        "おおとや三元豚と野菜の黒酢あん": "950円（税込）",
        "豚と野菜の塩麹炒め": "790円（税込）",
        "豚と野菜の豆鼓味噌炒め": "840円（税込）",
        "豚の生姜焼き": "790円（税込）",
        "おおとや三元豚のロースかつ": "980円（税込）",
        "プルコギ牛肉炒め": "980円（税込）",
        "さばの炭火焼き": "840円（税込）",
        "さばの竜田揚げ香味ねぎソース": "890円（税込）",
        "しまほっけの炭火焼き": "980円（税込）",
        "さばの味噌煮": "890円（税込）",
        "沖目鯛の醤油麹漬け炭火焼き": "980円（税込）",
        "牛プルコギの彩りサラダボウル": "940円（税込）",
        "バジルチキンの彩りサラダボウル": "890円（税込）",
        "ばくだん丼": "840円（税込）",
        "【まぐろ増量】ばくだん丼": "990円（税込）",
        "かあさんの玉子とじ": "940円（税込）",
        "チキン味噌かつ煮": "890円（税込）",
        "豆腐と鶏肉のトロトロ煮": "940円（税込）",
        "辛旨 豚キムチ鍋": "980円（税込）",
        "［サラダ］グリーンサラダ": "240円（税込）",
        "［サラダ］ひんやり豆腐サラダ": "290円（税込）",
        "［サラダ］千切りキャベツサラダ": "190円（税込）",
        "［小鉢］お豆腐ねばねば小鉢": "290円（税込）",
        "［小鉢］大戸屋風ばくだん小鉢": "290円（税込）",
        "［小鉢］ひんやり豆腐": "190円（税込）",
        "［小鉢］アカモク小鉢": "190円（税込）",
        "［サラダ］ポテトサラダ": "190円（税込）",
        "［小鉢］ひじきの煮物": "190円（税込）",
        "［小鉢］金平ごぼう": "190円（税込）",
        "［小鉢］ほうれん草の胡麻和え": "190円（税込）",
        "［おかず］ミニ野菜の黒酢あん": "290円（税込）",
        "［おかず］ミニ鶏の黒酢あん": "350円（税込）",
        "［おかず］ミニすけそう鱈の黒酢あん": "350円（税込）",
        "［おかず］ミニ豚の黒酢あん": "380円（税込）",
        "［おかず］かぼちゃコロッケ": "200円（税込）",
        "［おかず］ミニ香味唐揚げ": "200円（税込）",
        "［おかず］ミニさばの炭火焼き": "350円（税込）",
        "［おかず］ミニほっけの炭火焼き": "380円（税込）",
        "[ご飯]削りたて鰹本枯節のおかかごはんセット": "90円（税込）",
        "［ご飯のお供］きみだま": "80円（税込）",
        "［ご飯のお供］納豆": "90円（税込）",
        "［ご飯のお供］生たまご": "50円（税込）",
        "［ご飯のお供］とろろ": "110円（税込）",
        "[ご飯]削りたて鰹本枯節": "50円（税込）",
        "［ご飯］五穀ご飯(180g)": "190円（税込）",
        "［ご飯］ご飯(180g)": "190円（税込）",
        "［味噌汁］たっぷり野菜の麦みそ汁": "250円（税込）",
        "［味噌汁］": "70円（税込）",
        "お子様オムライスプレート": "390円（税込）",
        "お子様野菜カレー": "390円（税込）",
        "お子様うどんと唐揚げ": "390円（税込）",
        "大戸屋ティラミス　黒蜜きな粉": "290円（税込）",
        "たまごプリン": "290円（税込）",
        "もちもちコーヒーゼリー": "290円（税込）",
        "ミルクアイスクリーム": "190円（税込）",
        "抹茶アイスクリーム": "190円（税込）"
    }
}
       ]
   }
   },
//    mounted: function() {
//         var self = this;
//         axios
//             .get('.assets/shopdata.json')
//             .then(function(response) {
//                 self.shops = response.data;
//             })
//             .catch(function(error) {
//                 console.log('取得に失敗しました。', error);
//             })
//     }
};
</script>