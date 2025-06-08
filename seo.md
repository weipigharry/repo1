
<script>
//先載入完再跑JS
$(document).ready(function(){ //以下開始放Javascript
});
window.onload = function(){ //以下開始放Javascript
}
//先載入完ajax再跑JS
$(document).ajaxComplete(function() {  //以下開始放Javascript
});
	//抓整個網址
	var url_now = window.location.href;
	
	//抓取網址路徑
	var url_now = location.pathname.replace(/\//g,"");
	
	//運用函數
	var para_id = getParameter("id", url_now);
	var para_num = count_url(url_now);
	var num_id = Number(para_id); //字串轉數字
	
	//TDK變數
	var tag_title = document.getElementsByTagName("title")[0];
	var meta_des = document.getElementsByName("description")[0];
	var meta_key = document.getElementsByName("keywords")[0];

	console.log("TEST")

	//錨文本陣列
	var indexanchors = ["教主醫美","教主醫美診所","教主醫美整形外科","台北教主醫美","台中教主醫美"]; 
	
	//網址解碼(解中文編碼)
	decodeURIComponent(url_now);
	//去除空白
	.replace(/\s/g, '')
	//去除斷行
	.replace(/(?:\r\n|\r|\n)/g, '')
	//去除左右空白
	.replace(/(^[\s]*)|([\s]*$)/g, "")
	//去除空格
	.replace(/&nbsp;/ig, "")
	//去除左右空白
	.trim()

	switch (expression)
	{
	case label1:
	  expression = label1 时执行的代码 ;
	  break;  
	case label2:
	  expression = label2 时执行的代码 ;
	  break;
	default:
	  表达式的值不等于 label1 及 label2 时执行的代码;
	}

	//改TDK(if判斷:符合全部網址)
	if(window.location.href == "http://www.p-v-b.com.tw/page.php?menu_id=21"){
		tag_title.innerHTML = "";
		meta_des.content = "";
		meta_key.content = "";
	}
	
	//改TDK(if判斷:符合部分網址)
	if(document.URL.includes("online.php?label=37")){
		tag_title.innerHTML = "";
		meta_des.content = "";
		meta_key.content = "";
	}
	
	//設TDK之函數
	function setTD(strTitle, strDes, strKey){
		document.getElementsByTagName("title")[0].innerHTML = strTitle;
		document.getElementsByName("description")[0].content = strDes;
		document.getElementsByName("keywords")[0].content = strKey;
	}
	//創造Description之函數 (沒有標籤時)
	function createDescription(text){
		var meta_descr = document.createElement("meta");
			meta_descr.name = "description";
			meta_descr.content = text;
		var head_root = document.getElementsByTagName("head")[0];
			head_root.appendChild(meta_descr);
	}
	//內鍊物件分類之寫法
	var stoolData = {group:[
		{pageName:"台北抽水肥", pageUrl:"/paper.asp?id=66&g=27", page_anchors:["台北抽水肥推薦","台北抽水肥公司","專業台北抽水肥","台北抽水肥工程"]},
		{pageName:"新北抽水肥", pageUrl:"/paper.asp?id=67&g=27", page_anchors:["新北抽水肥工程","新北抽水肥推薦","新北抽水肥公司","專業新北抽水肥"]},
		{pageName:"基隆抽水肥", pageUrl:"/paper.asp?id=68&g=27", page_anchors:["專業基隆抽水肥","基隆抽水肥工程","基隆抽水肥推薦","基隆抽水肥公司"]},
		{pageName:"桃園抽水肥", pageUrl:"/paper.asp?id=12&g=27", page_anchors:["桃園抽水肥公司","專業桃園抽水肥","桃園抽水肥工程","桃園抽水肥推薦"]},
		{pageName:"新竹抽水肥", pageUrl:"/paper.asp?id=69&g=27", page_anchors:["新竹抽水肥推薦","新竹抽水肥公司","專業新竹抽水肥","新竹抽水肥工程"]}
	]};
	var toiletData = {group:[
		{pageName:"台北通馬桶", pageUrl:"/paper.asp?id=50&g=28", page_anchors:["專業台北通馬桶","台北通馬桶公司","台北通馬桶工程","台北通馬桶推薦"]},
		{pageName:"基隆通馬桶", pageUrl:"/paper.asp?id=64&g=28", page_anchors:["基隆通馬桶推薦","專業基隆通馬桶","基隆通馬桶公司","基隆通馬桶工程"]},
		{pageName:"桃園通馬桶", pageUrl:"/paper.asp?id=51&g=28", page_anchors:["桃園通馬桶工程","桃園通馬桶推薦","專業桃園通馬桶","桃園通馬桶公司"]},
		{pageName:"新竹通馬桶", pageUrl:"/paper.asp?id=65&g=28", page_anchors:["新竹通馬桶公司","新竹通馬桶工程","新竹通馬桶推薦","專業新竹通馬桶"]}
	]};

	setInnerLink(document.getElementsByClassName("ac03_line01b2")[0], stoolData.group[para_id%stoolData.group.length].pageUrl, stoolData.group[para_id%stoolData.group.length].page_anchors[para_id%stoolData.group[para_id%stoolData.group.length].page_anchors.length], toiletData.group[para_id%toiletData.group.length].pageUrl, toiletData.group[para_id%toiletData.group.length].page_anchors[para_id%toiletData.group[para_id%toiletData.group.length].page_anchors.length]);	

	//物件判斷暫存(Ted寫法)
	var object = {group:[
			{"yes":326},
			{}
		]}
	var property = "detailID"

	if(property in object.group[0]){

	}
	if(target){

	}

	//加內鍊之函數
	function setInternalLink(place, href1, anchor1, href2, anchor2){
		var node = document.createElement("p");
			node.style.textAlign = "center";
			node.style.fontFamily = "微軟正黑體";
			node.style.fontSize = "12px";
			node.innerHTML = '相關資訊：<span id="js_anchor"></span>｜<span id="js_anchor2"></span>';

		place.appendChild(node);
		document.getElementById("js_anchor").innerHTML = '<a href="'+href1+'">'+anchor1+'</a>';
		document.getElementById("js_anchor2").innerHTML = '<a href="'+href2+'">'+anchor2+'</a>';
	}

	//內鍊加在最上方
	function setUpperInternalLink(place, href1, anchor1, href2, anchor2){
		var node = document.createElement("p");
			node.style.textAlign = "center";
			node.style.fontFamily = "微軟正黑體";
			node.style.fontSize = "12px";
			node.innerHTML = '相關資訊：<span id="js_anchor"></span>｜<span id="js_anchor2"></span>';

		place.insertBefore(node, place.childNodes[0]);
		document.getElementById("js_anchor").innerHTML = '<a href="'+href1+'">'+anchor1+'</a>';
		document.getElementById("js_anchor2").innerHTML = '<a href="'+href2+'">'+anchor2+'</a>';
	}

	//加h標籤之函數
	function setH1(place, text1){
		var h1_tag = document.createElement("h1");
			h1_tag.style.textAlign = "center";
			h1_tag.style.fontFamily = "微軟正黑體";
			h1_tag.style.fontSize = "16px";
			h1_tag.style.fontWeight = "bold";
			h1_tag.style.marginTop = "0px";
			h1_tag.innerHTML = text1;
		var list = place;
			list.insertBefore(h1_tag, list.childNodes[0]);
	}
	
	//加麵包屑之函數 (insertBefore的用法)
	function createBreadcrumb(place, href1, text1, href2, text2){
		var bread = document.createElement("p");
			bread.id = "crumb";
		var list = place;
			list.insertBefore(bread, list.childNodes[0]);
		document.getElementById("crumb").innerHTML = '<a href="/">首頁</a> > <a href="'+href1+'">'+text1+'</a> > <a href="'+href2+'">'+text2+'</a>';
	}

	//改寫麵包屑連結
	function resetBreadcrumb(href1, text1, href2, text2){
		document.querySelector("ol.breadcrumb").innerHTML = '<li><a href="/chinese/index.html" class="poshome" title="首頁">首頁</a></li><li><a href="/chinese/showroom1.html" title="products">商品櫥窗</a></li><li><a href="'+href1+'">'+text1+'</a></li><li><a href="'+href2+'">'+text2+'</a></li>';
	}

	//插入details、summary之函數
	function createContent(place, text1, text2){
		var node = document.createElement("p");
			node.style.fontFamily = "微軟正黑體";
			node.style.fontSize = "12px";
			node.innerHTML = '<details><summary>'+text1+'</summary>'+text2+'</details>';

		place.appendChild(node);
	}

	// 消除details的箭頭
	function replace_triangle(){
		var title_style = document.createElement("style");
			title_style.innerHTML = 'details summary::-webkit-details-marker { display:none; }	details > summary:first-of-type {list-style-type: none;}';
		var head_root = document.getElementsByTagName("head")[0];
			head_root.appendChild(title_style);
	}

	function createDetailContent(target, id, content){
		var real_id = "jsContent"+id;
		target.innerHTML = '<span onclick="show(\''+real_id+'\')">'+target+'</span>';
		var tag_article = document.createElement("article");
			tag_article.style.display = "none";
			tag_article.style.textAlign = "center";
			tag_article.id = real_id;
			tag_article.innerHTML = content;
		target.parentNode.insertBefore(tag_article, target.nextElementSibling);

	}

	function show(id){
		var t = document.querySelector("article#"+id);
			t.style.display = (t.style.display == "none") ? "":"none";
	}

	//圖片alt標籤之函數
	function createImgAlt(text, anchors){
		var img = document.getElementsByTagName("img");
		for(var i=0;i<img.length;i++){
			img[i].alt = text + anchors[i%anchors.length];
		}
	}

	//加canonical標籤之函數
	function setCanonical(url_path){
		var link_seo = document.createElement("link");
			link_seo.rel = "canonical";
			link_seo.href = url_path;
		var head_place = document.getElementsByTagName("head")[0];
			head_place.appendChild(link_seo);
	}

	//加hreflang標籤之函數
	function setHrefLang(lang,url_path){
		var link_seo = document.createElement("link");
			link_seo.rel = "alternate";
			link_seo.hreflang = lang;
			link_seo.href = url_path;
		var head_place = document.getElementsByTagName("head")[0];
			head_place.appendChild(link_seo);
	}
	
	//加prev、next標籤之函數
	function setPrevNext(path_next, path_prev){
		var link_next = document.createElement("link");
			link_next.rel = "next";
			link_next.href = path_next;
		var link_prev = document.createElement("link");
			link_prev.rel = "prev";
			link_prev.href = path_prev;
		var head_place = document.getElementsByTagName("head")[0];
			head_place.appendChild(link_next);
			head_place.appendChild(link_prev);
	}
	
	//抓取網址中特定之參數
	function getParameter(name, url){
		name = name.replace(/[\[\]]/g, "\\$&");
		var regex = new RegExp("[?&]" + name + "(=([^&#]*)|&|#|$)");
		var results = regex.exec(url);
		if(!results){
			return null;
		}
		if(!results[2]){
			return ' ';	
		}
		return decodeURIComponent(results[2].replace(/\+/g, " "));
	}

	//將網址化為數字 (搭配url_now)
	function count_url(url){
		var url_to_id = 0;
		for(var i=0 ; i<url.length ; i++){
			url_to_id = url_to_id+url.charCodeAt(i);
		}
		return url_to_id;
	}
	
	//加Schema之函數
	function addSchema(schema){
		var scriptJSON = document.createElement("script");
			scriptJSON.type = 'application/ld+json';
			scriptJSON.innerHTML = JSON.stringify(schema);
		document.getElementsByTagName("head")[0].appendChild(scriptJSON);
	}
	//配合QA、麵包屑Schema使用
	function extend(obj, src) {
		for (var key in src) {
			if (src.hasOwnProperty(key)) obj[key] = src[key];
		}
	}

	//麵包屑Schema之函數
	function setBreadcrumbSchema(place){
		var schemaData_bread = {
			"@context": "http://schema.org",
			"@type": "BreadcrumbList",
			"itemListElement": []
		}
		
		//先把a連結抓出來(陣列形式)
		var tag_li_breadcrumb = place.getElementsByTagName("a");
		
		var itemListElement = [];
		for(var i=0 ; i<tag_li_breadcrumb.length ; i++){
			var item = {
				"@type": "ListItem",
				"position": i+1,
				"item": {
					"@id": tag_li_breadcrumb[i].href,
					"name": tag_li_breadcrumb[i].textContent,
				}
			};
			itemListElement.push(item);
		}
		extend(schemaData_bread.itemListElement, itemListElement);
		addSchema(schemaData_bread);
	}
	
	//產品schema之函數
	function setProductSchema(){
		//產品名
		var product_name = document.getElementsByClassName("title")[0].textContent;
		//產品價格
		var product_price = document.getElementById("recommanded-price").textContent.replace(/(^[\s]*)|([\s]*$)/g, "").split("$")[1];
		//商品圖網址
		var img_url = document.getElementsByTagName("img")[5].src;
	
		var schemaData_product = {
			"@context": "http://www.schema.org",
			"@type": "product",
			"brand": "la yoo 來喲",
			"name": product_name,
			"image": img_url,
			"description": "la yoo來喲專賣"+product_name+"，手工製作高質感"+product_name+"，"+product_name+"推薦la yoo來喲。",
			"offers": {
				"@type": "Offer",
				"availability": "http://schema.org/InStock",
				"price": product_price,
				"priceCurrency": "TWD"
			},
			"aggregateRating": {
				"@type": "aggregateRating",
				"ratingValue": 5-(para_num%10)/10,  //星星數：4.1~5
				"reviewCount": 300-(para_num%50)  //評論數：251~300
			}
		}
		addSchema(schemaData_product);
	}

	// 此結構化資料限制「網站發布了常見問題內容，且並未開放使用者提交其他答案」
	// https://developers.google.com/search/docs/data-types/faqpage?hl=zh-tw
	// 如果是「網站有讓使用者回答單一問題的設計」請參考連結：QA結構化資料
	// https://developers.google.com/search/docs/data-types/qapage?hl=zh-tw
	function setFAQSchema(){
		var schemaData_FAQ = {
			"@context": "http://schema.org",
			"@type": "FAQPage",
			"mainEntity": []
		};
		var questionList = [];
		for(var i=0 ; i<document.querySelectorAll(".accordion").length ; i++){ //問題總數
			var item = {
				"@type": "Question",
				"name": document.querySelectorAll(".accordion .title")[i].innerText.replace("Q：",""), //問題名稱
				"acceptedAnswer": {
					"@type": "Answer",
					"text": document.querySelectorAll(".accordion .answer")[i].innerText.replace("A：","") //問題答案
				}
			};
			questionList.push(item);
		}
		extend(schemaData_FAQ.mainEntity, questionList);
		addSchema(schemaData_FAQ);
	}
	function setFixedFAQSchema(){
		var schemaData_faq = {
			"@context": "http://www.schema.org",
			"@type": "FAQPage",
			"mainEntity":[{
				"@type":"Question",
				"name":"預約的剪燙髮方式？",
				"acceptedAnswer":{
					"@type":"Answer",
					"text":"為維護良好的服務品質我們是採預約制，平日建議2~3天前預約，假日3~5天前預約較能安排您想預約的時間。最晚預約時間:剪髮/護髮是6:00、染髮是5:00(不包含去色)、燙髮是3:30的時間。可透過電話、官網、LINE、或是粉絲團私訊預約。"
				}
			},
			{
				"@type":"Question",
				"name":"剪燙髮的收費方式？",
				"acceptedAnswer":{
					"@type":"Answer",
					"text":"剪髮價位依照設計師個人剪髮價位收費，燙/染/護髮會依照頭髮長度所需的用量收費,所以長髮的費用會較多一些。本店採分項計費,避免同時多種項目時有費用重疊的部分，結帳方式可使用現金、信用卡、手機支付(Apple Pay)都可以的。"
				}
			},
			{
				"@type":"Question",
				"name":"Rainbow Hair使用的產品有哪些？",
				"acceptedAnswer":{
					"@type":"Answer",
					"text":"店內使用的產品皆為國際知名品牌，享有品質保證及技術指導；洗髮產品—義大利品牌達芬妮絲，講求溫和植萃低敏成份、護髮產品—日本哥德式，使用頂級MILBON系列產品達到髮質保水修復度、燙髮產品—日本哥德式，知名品牌藥水品質穩定燙髮效果好、染髮產品—巴黎萊雅，色彩飽和度及髮質效果兼俱"
				}
			}]
		}
		addSchema(schemaData_faq);
	}

	//彙整頁中抓細節頁資料 (化為陣列)
	function getDetailData(){
		var array = [];
		for(var i=0;i<document.querySelectorAll("div.itemTitle > a").length;i++){
			var new_url = document.querySelectorAll("div.itemTitle > a")[i].href
			var id = new_url.split("/")[6];
			//var text = document.querySelectorAll("div.itemTitle > a")[i].textContent;
			array.push(id);
		}
		var uniq = [...new Set(array)];  //抓到複數元素時，刪除重複元素
		console.log(array);	
	}

/* 以下為Ted版本 */


	/////
/* 常處理的SEO事項 */

	// <!-- 計算URL -->
	function count_url(url){
		var url_to_id = 0;
		for(var i=0 ; i<url.length ; i++){
			url_to_id += url.charCodeAt(i);
		}
		return url_to_id;
	}


	// <!-- 取URL參數 -->
	function getParameter(name,url){
		name = name.replace(/[\[\]]/g, "\\$&");
		var regex = new RegExp("[?&]" + name + "(=([^&#]*)|&|#|$)");
		var results = regex.exec(url);
		if(!results){
			return null;
		}
		if(!results[2]){
			return ' ';
		}
		return decodeURIComponent(results[2].replace(/\+/g, " "));
	}


	// <!-- insert after -->
	referenceNode.parentNode.insertBefore(newNode, referenceNode.nextElementSibling);


	// <!-- 內鏈區塊 -->
	function setInternalLink(target, href1, anchor1, href2, anchor2){

		var tagDiv = document.createElement("div");
		tagDiv.style.marginTop = "2.5em";
		tagDiv.style.textAlign = "center";
		tagDiv.innerHTML = '<span>更多資訊</span>：<a style="color:#555" href="'+href1+'">'+anchor1+'</a>｜<a style="color:#555" href="'+href2+'">'+anchor2+'</a>';
		target.appendChild(tagDiv);

	}


	// <!-- 內鏈區塊彈性版 -->
	function setInternalLink(target){

		var tagDiv = document.createElement("div");
		tagDiv.style.marginTop = "2.5em";
		tagDiv.style.textAlign = "center";
		tagDiv.style.color = "#6b5a29";

		var strLink = "";
		for(var i=1 ; i<arguments.length ; i++){
			strLink += '<a style="color:#6b5a29;" href="'+arguments[i].href+'">'+arguments[i].anchor+'</a>｜';
		}

		tagDiv.innerHTML = '<span id="innerLink">更多資訊</span>：'+strLink.substring(0, strLink.length-1);
		target.appendChild(tagDiv);
	}


	// 內鏈用
	var objLink = {link: [
			{href: "", anchor: []},
			{href: "", anchor: []},
			{href: "", anchor: []},
			{href: "", anchor: []}
	]};


	// <!-- 建link標籤 -->
	function create_tag_link(rel, href){
		var tag_head = document.getElementsByTagName("head")[0];
		var tag_link = document.createElement("link");
			tag_link.rel = rel;
			tag_link.href = href;
		tag_head.appendChild(tag_link);
	}

	// {attrName: "", attrValue: ""}
	// createTag("link", {rel: "canonical", href: ""});
	function createTag(tagName) {
		var tag_head = document.getElementsByTagName("head")[0];
		var tag = document.createElement(tagName);

		for (var i = 1; i < arguments.length; i++) {
			for(attr in arguments[i]){
				tag.setAttribute(attr, arguments[i][attr]);
			}
		}
		tag_head.appendChild(tag);
	}


	// <!-- 設定TD -->
	/* 一定要放title的string哦 */
	function setTDA(){
		if(arguments.length > 1){
			if(!document.querySelector("meta[name='description']")){
				var metaDes = document.createElement("meta");
				metaDes.name = "description";
				document.getElementsByTagName("head")[0].appendChild(metaDes);
			}
			document.getElementsByTagName("title")[0].innerHTML = arguments[0];
			document.getElementsByName("description")[0].content = arguments[1];
		}else{
			document.getElementsByTagName("title")[0].innerHTML = arguments[0];
		}
	}

	function setTD(){
		var metaTitle = document.querySelector("title");
		var metaDes = document.querySelector("meta[name='description']");

		if(arguments.length > 1){
			if(!metaDes){
				var des = document.createElement("meta");
				des.name = "description";
				document.getElementsByTagName("head")[0].appendChild(des);
			}
			metaTitle.innerHTML = arguments[0];
			metaDes.content = arguments[1];
		}
		else{
			metaTitle.innerHTML = arguments[0];
		}
	}

	// <!-- set Social Media meta -->
	// {cond: "", cont: ""} meta[property='og:title']
	function setSocialMediaMeta(){
		for(var i=0 ; i<arguments.length ; i++){
			document.querySelector(arguments[i].cond).content = arguments[i].cont;
		}
	}

	// <!-- 設定年份 -->
	var year = getYear();
	function getYear(){
		var d = new Date();
		return d.getFullYear();
	}

	// <!-- Title替換頻率 -->
	function changeTitle(array){
		var strT = "";
		for(var i=0 ; i<array.length ; i++){
			if(i == array.length-1){
				strT += array[i];
			}else{
				strT += array[i]+"｜";
			}
		}
		return strT;
	}

	function combineArray(){
		var id = getID();
		var arrayT = [];
		for(var i=0 ; i<arguments.length ; i++){
			arrayT.push(arguments[i][id%arguments[i].length]);
		}
		return arrayT;
	}

	function getID(){
		var dateObj = new Date();
		if(dateObj.getDate() > 14){
			return dateObj.getMonth()+2;
		}else{
			return dateObj.getMonth();
		}
	}

	// <!-- 增加內容 -->
	function createDetailContent(content){
		var tagSpan = document.querySelector("div#innerLink span");
		tagSpan.innerHTML = '<a style="color:black; text-decoration: none;" id="jsTitle" href="#jsContent">更多資訊</a>';

		var tag_article = document.createElement("article");
		tag_article.style.display = "none";
		tag_article.id = "jsContent";
		tag_article.style.marginTop = "1em";
		tag_article.style.cssFloat = "left";
		tag_article.innerHTML = content;
		document.querySelector("#exh_left_tool").appendChild(tag_article);
	}

	$(document).ready(function(){

	    $("#jsTitle").click(function(event){
	        event.preventDefault();
	        $("#jsContent").toggle();
	    });

	});

	function createDetailContent(target, id, content){
		target.innerHTML = '<span><a id="jsTitle'+id+'" href="#jsContent'+id+'" style="color:#444444">'+target.textContent+'</a></span>';
		var tag_article = document.createElement("article");
			tag_article.style.display = "none";
			tag_article.style.textAlign = "center";
			tag_article.id = "jsContent"+id;
			tag_article.innerHTML = content;
		target.parentNode.insertBefore(tag_article, target.nextElementSibling);
	}

	function createDetailContent(target, id, content){
		var real_id = "jsContent"+id;
		target.innerHTML = '<span onclick="show(\''+real_id+'\')">'+target.textContent+'</span>';
		var tag_article = document.createElement("article");
			tag_article.style.display = "none";
			tag_article.style.textAlign = "center";
			tag_article.id = real_id;
			tag_article.innerHTML = content;
		target.parentNode.insertBefore(tag_article, target.nextElementSibling);
	}

	function show(id){
		var t = document.querySelector("article#"+id);
			t.style.display = (t.style.display == "none") ? "":"none";
	}


	// <!-- Prev Next -->
	/*
		1. 確認有沒有分頁的情況
		2. 判斷是否為第一頁
		3. 判斷是否為最後一頁
		4. 中間頁的情況
	*/


/////
/* 常處理的SEO事項 -> 字串處理 + JQuery */

	// <!-- 去除斷行 / 去除空格 ； 中文 ； 截文字 ； match ； lowerCase -->
	des.replace(/(?:\r\n|\r|\n|\s+)/g, '');
	des.replace(/[\u4e00-\u9fa5]/g, '-');
	des.replace(/(?:\r\n|\r|\n|\s+)/g, '').slice(0,100);
	des.match(/\d{4}\/\d{2}\/\d{2}/g)[0];
	str.toLowerCase();


	// <!-- 去除Tag -->
	function removeTag (strText){
	    var regEx = /(<p)(.*)(\/p>)/g;
	    var string = strText.replace(regEx, "");
	 	var regEx2 = /(<h2)(.*)(\/h2>)/g;
	 	var string2 = string.replace(regEx2, "");
	    return string2.replace(/<[^>]*>/g, '').replace(/(?:\r\n|\r|\n|\s+)/g, '').trim();
	}


	// <!-- After AJAX -->
	$( document ).ajaxComplete(function() {
	  $( ".log" ).text( "Triggered ajaxComplete handler." );
	});

	$( document ).ready(function() {
	    console.log( "ready!" );
	});


	// <!-- 伸縮面板 -->
	$(document).ready(function(){
		$(".travellist__maintitle").click(function(event){
			event.preventDefault();
			$("#kpn").toggle();
		});
	});


/////
/* 常處理的SEO事項 -> 語意標籤 */

	// <!-- add Schema + breadCrumb Schema -->
	function addSchema(schema){
		var scriptJSON = document.createElement("script");
		scriptJSON.type = 'application/ld+json';
		scriptJSON.innerHTML = JSON.stringify(schema);
		document.getElementsByTagName("head")[0].appendChild(scriptJSON);
	}

	function extend(obj, src) {
	    for (var key in src) {
	        if (src.hasOwnProperty(key)) obj[key] = src[key];
	    }
	}

	function setBreadCrumbSchema(breadContent){
		var schemaData_bread = {
			"@context": "http://schema.org",
			"@type": "BreadcrumbList",
			"itemListElement": []
		};
		var itemListElement = [];
		for(var i=0 ; i<breadContent.length ; i++){
			var item = {
				"@type": "ListItem",
				"position": i+1,
				"item": {
					"@id": breadContent[i].href,
					"name": breadContent[i].anchor
				}
			};
			itemListElement.push(item);
		}
		extend(schemaData_bread.itemListElement, itemListElement);
		addSchema(schemaData_bread);
	}


	// <!-- Event Schema -->
	var schemaData_event = {
	  "@context": "http://schema.org",
	  "@type": "Event",
	  "name": "Jan Lieberman Concert Series: Journey in Jazz",
	  "startDate": "2018-10-01T19:30-08:00",
	  "location": {
	    "@type": "Place",
	    "name": "Santa Clara City Library, Central Park Library",
	    "address": {
	      "@type": "PostalAddress",
	      "streetAddress": "2635 Homestead Rd",
	      "addressLocality": "Santa Clara",
	      "postalCode": "95051",
	      "addressRegion": "CA",
	      "addressCountry": "US"
	    }
	  },
	  "image": [
	    "https://example.com/photos/1x1/photo.jpg"
	   ],
	  "description": "",
	  "endDate": "2019-01-01T23:00-08:00",
	  "offers": {
	    "@type": "Offer",
	    "url": "https://www.example.com/event_offer/12345_201803180430",
	    "price": "30",
	    "priceCurrency": "USD",
	    "availability": "http://schema.org/InStock",
	    "validFrom": "2017-01-20T16:20-08:00"
	  },
	  "performer": {
	    "@type": "PerformingGroup",
	    "name": "Andy Lagunoff"
	  }
	}


	// <!-- Carousel Schema -->
	var schemaData_carousel = {
	  "@context":"http://schema.org",
	  "@type":"ItemList",
	  "itemListElement":[
	    {
	      "@type":"ListItem",
	      "position":1,
	      "url":"https://www.auroratour.com.tw/news.php?c=1"
	    },
	    {
	      "@type":"ListItem",
	      "position":2,
	      "url":"https://www.auroratour.com.tw/news.php?c=4"
	    }
	  ]
	};


	// <!-- Article Schema -->
	var schemaData_article = {
		"@context": "http://schema.org",
		"@type": "Article",
		"mainEntityOfPage": {
	    	"@type": "WebPage",
	    	"@id": url_now
	  	},
		"headline": tag_h2_text,
		"image":"",
		"datePublished": "",
		"author": {
	    	"@type": "Organization",
	    	"name": "吉光旅遊 ‧ 東煒旅行社"
	  	},
	   	"publisher": {
	    	"@type": "Organization",
	    	"name": "吉光旅遊 ‧ 東煒旅行社",
	    	"logo": {
	      		"@type": "ImageObject",
	      		"url": "http://www.auroratour.com.tw/images/logo.jpg"
	    	}
	  	},
	  	"description": "..."
	};


	// <!-- Product Schema -->
	var schemaData_product = {
		"@context": "http://schema.org/",
		"@type": "Product",
		"name": parameter,
		"image": parameter,
		"description": parameter,
		"brand": {
    		"@type": "Thing",
    		"name": "ZOOPER (台灣公司)旌宇企業總代理"
  		},
   		"aggregateRating": {
    		"@type": "AggregateRating",
    		"ratingValue": 5-(url_id%10)/10,
    		"reviewCount": Math.floor(count_url(obj_data.group[i].prodCd[j])/10)
  		},
		"offers": {
    	"@type": "Offer",
    	"priceCurrency": "NTD",
    	"price": document.getElementsByClassName("price")[0].textContent.replace(/[,\$]/g, ""),
    	//document.querySelector("li.price_content").textContent.replace(/[^\d]/g, '')
    	"itemCondition": "NewCondition",
    	"availability": "InStock"
 		 }
	};


	// <!-- BreadCrumb Schema 寫死-->
	var schemaData_bread = {
	  "@context": "http://schema.org",
	  "@type": "BreadcrumbList",
	  "itemListElement": [{
	    "@type": "ListItem",
	    "position": 1,
	    "item": {
	      "@id": "http://www.loyaltytour.com.tw/",
	      "name": "誠旺旅行社"
	    }
	  },{
	    "@type": "ListItem",
	    "position": 2,
	    "item": {
	      "@id": "",
	      "name": ""
	    }
	  }]
	};


	// <!-- LocalBusiness Schema -->
	var schemaData_localbusiness = {
		  "@context": "http://www.schema.org",
		  "@type": "TravelAgency",
		  "name": "吉光旅遊",
		  "url": "https://www.auroratour.com.tw/",
		  "logo": "https://www.auroratour.com.tw/images/logo.svg",
		  "image": "",
		  "description": "",
		  "address": {
		    "@type": "PostalAddress",
		    "streetAddress": "台北市大同區承德路一段69巷5號",
		    "addressLocality": "大同區",
		    "addressRegion": "台北市",
		    "postalCode": "103",
		    "addressCountry": "台灣"
		  },
	      "hasOfferCatalog": {
	      	"@type": "OfferCatalog",
	      	"name": "",
	      	"itemListElement": [
		      	{
		      	  "@type": "Offer",
		      	  "itemOffered": {
		      	    "@type": "Service",
		      	    "name": "日本深度旅遊團"
		      	  }
		      	},
		      	{
		      	  "@type": "Offer",
		      	  "itemOffered": {
		      	    "@type": "Service",
		      	    "name": "國外團體旅遊"
		      	  }
		      	}
	      	]
	      },
	      "sameAs": [
      	  ],
		  "hasMap": "https://goo.gl/maps/KdvTdvLAonB2",
		  "openingHours": "Mo, Tu, We, Th, Fr 09:00-18:00",
		  "telephone": "+886-2-25582525",
		  "contactPoint": {
		    "@type": "ContactPoint",
		    "telephone": "+886-2-25582525",
		    "contactType": "Sales"
		  }
		};

	// LocalBusiness multi place 或 參考晴天旅遊
	var schemaData_localbusiness = {
	  "@context": "http://schema.org/",
	  "@graph": [
	    {
	      "@id": "#MainOrganization",
	      "@type": "Organization",
	      "name": "",
	      "url": "",
	      "logo": "",
	      "description": "",
	      "hasOfferCatalog": {
	      	"@type": "OfferCatalog",
	      	"name": "",
	      	"itemListElement": [
		      	{
		      	  "@type": "Offer",
		      	  "itemOffered": {
		      	    "@type": "Service",
		      	    "name": ""
		      	  }
		      	}
	      	]
	      },
	      "sameAs": [
	        ""
	      ]
	    },
	    {
	      "@type": "ProfessionalService",
	      "parentOrganization": {
	        "@id": "#MainOrganization"
	      },
	      "name": "新絲路留遊學",
	      "address": {
	        "@type": "PostalAddress",
	        "streetAddress": "開封街一段66號3樓",
	        "addressLocality": "中正區",
	        "addressRegion": "台北市",
	        "postalCode": "100",
	        "telephone": "0277305686"
	      },
	      "openingHours": [
	        "Mo-Fr 09:30-18:30"
	      ],
	      "image": "https://www.iae-taiwan.net/images/logo/top_logo.png",
	      "hasmap": "https://goo.gl/maps/NCzbJXmzQ1N2"
	    },
	    {
	    	"..."
	    }
	  ]
	};


	// <!-- FAQ Page Schema -->
	var schemaData_faqpage = {
		"@context": "https://schema.org",
		"@type": "FAQPage",
		"mainEntity": [{
		  "@type": "Question",
		  "name": "What is the return policy?",
		  "acceptedAnswer": {
		    "@type": "Answer",
		    "text": "..."
		  }
		}, {
		  "@type": "Question",
		  "name": "",
		  "acceptedAnswer": {
		    "@type": "Answer",
		    "text": "..."
		  }
		}]
	};

/////
/* 常用協助整理SEO事項 */

	// <!-- array to objec -->
	function toObject(arr,val){
		var obj = {};
		for(var i=0 ; i<arr.length ; i++){
			obj[arr[i]] = val;
		}
		return obj;
	}

	// <!-- 抓 Google 推薦字詞 -->
	var tt = document.querySelectorAll("div.card-section")[0];
	var ss = tt.querySelectorAll("a");
	var arrayData = [];
	for(var i=0 ; i<ss.length ; i++){
		console.log(ss[i].textContent);
		arrayData.push(ss[i].textContent);
	}
	console.log(arrayData);
	JSON.stringify(arrayData,"\b");

	// <!-- 抓 Google 搜尋框推薦字詞 -->
	var vv = document.querySelectorAll("div.suggestions-inner-container span");
	var arrayData2 = [];
	for(var i=0 ; i<vv.length ; i++){
		console.log(vv[i].textContent);
		arrayData2.push(vv[i].textContent);
	}
	console.log(arrayData2);
	JSON.stringify(arrayData2,"\b");

	// <!-- 抓 Google 搜尋結果 -->
	var results_title = document.querySelectorAll("h3.LC20lb");
	var results_url = document.querySelectorAll("cite.iUh30");

	for(var i=0 ; i<results_title.length ; i++){
		// var str = results_title[i].textContent+'<br>'+results_url[i].textContent+'<br>-------------<br>';
		// console.log(str);
		console.log(results_title[i].textContent);
		console.log(results_url[i].textContent);
		console.log("-------------");
	}

	// <!-- GTM 自訂變數 -->
	// VAR_XXXX
	function (){
		var url = [];
		for(var i=0 ; i<url.length ; i++){
			if(window.location.href.split("/")[3] == url[i]){
				return "燈具知識";
			}
		}
	}


	// <!-- 取得連結程式中的KW -->
	var group_id = [2,3,5,10,19];
	getKW(group_id);

	function getKW(group){
		var kwList = "";
		for(var i=0 ; i<group.length ; i++){
			var target = 'div[group_id="'+group[i]+'"]';
			var targetGroup = document.querySelector(target);

			for(var j=0 ; j<targetGroup.querySelectorAll("input[name='keywords']").length ; j++){
				kwList += targetGroup.querySelectorAll("input[name='keywords']")[j].value+'\n';
			};
		}
		return kwList;
	}

	// <!-- GSC 資料加總 -->
	var t = document.querySelectorAll("table.i3WFpf")[3].querySelectorAll('tr[style=""]')

	var num = 0;
	for(var i=0 ; i<t.length ; i++){
		num += parseInt(t[i].querySelector('td[data-column-toggle-label="IMPRESSIONS"]').textContent.replace(/[,\$]/g, ""));
	}
	console.log(num);

	// <!-- 陣列處理 -->
	a.concat();
	a.indexOf();
	var origin = ["中美", "北美", "南美", "北美", "南美", "中美"];

	var result = origin.filter(function(element, index, arr){
		return arr.indexOf(element) === index;
	});

	console.log(result);
	// array.includes --> chrome 47才可以用


	// <!-- 整理字詞的函式 -->

	function sortOut(arrays){
		var arrayAll = [];
		for(var i=0 ; i<arguments.length ; i++){
			arrayAll = arrayAll.concat(arguments[i]);
		}
		console.log(arrayAll);
		var result = [];

		for(var j=0 ; j<arrayAll.length ; j++){
			if(j==0){
				result.push(addNewRow(arrayAll[0].href, arrayAll[0].anchor));
			}
			else{
				var isExist = compareObj(arrayAll[j], result);
				console.log(j ,isExist);
				if(isExist || isExist==0){ // 加入既有的anchor陣列
					// 0 是falsy值
					result[isExist].anchor.push(arrayAll[j].anchor);
				}
				else{ // 直接加入那一個Obj
					result.push(addNewRow(arrayAll[j].href, arrayAll[j].anchor));
				}
			}
		}
		// return arrayAll;
		return result;
	}

	function compareObj(objNow, arrayCompare){
		var target = Object.values(objNow); // ["href value", "anchor value"]

		for(var i=0 ; i<arrayCompare.length ; i++){
			if(target[0] == Object.values(arrayCompare[i])[0]){
				return i;
			}
		}
	}

	function addNewRow(href, anchor){
		var newObj ={};
			newObj.href = href;
			newObj.anchor = [anchor];
		return newObj;
	}
	JSON.stringify(sortOut(a1, a2));



/////
/* 其他 */

	// <!-- 時間處理 -->
	var getMonthWeek = function(a, b, c) {
		var date = new Date(a, parseInt(b) - 1, c),
			w = date.getDay(),
			d = date.getDate();
		return Math.ceil((d + 6 - w) / 7);
	};

	var getYearWeek = function(a, b, c) {
		var date1 = new Date(a, parseInt(b) - 1, c),
			date2 = new Date(a, 0, 1),
			d = Math.round((date1.valueOf() - date2.valueOf()) / 86400000);
		return Math.ceil((d + ((date2.getDay() + 1) - 1)) / 7);
	};

	var today = new Date(); //获取当前时间
	var y = today.getFullYear();
	var m = today.getMonth() + 1;
	var d = today.getDate();
	console.log("今天是：", y, "-", m, "-", d, "<br/>");
	console.log("今天是", y, "年的第 ", getYearWeek(y, m, d), " 周<br/>");
	console.log("今天是", m, "月的第 ", getMonthWeek(y, m, d), " 周<br/>");


	// <!-- 替換連結程式 -->
	var t = document.querySelectorAll("input[name='url']");

	for(var i=0 ; i<t.length ; i++){
		t[i].value = t[i].value.replace("/product/","/page.php?menu_id=3");
	}


	// <!-- indexOf vs for loop -->
	function Pe(){};
		var len = 1000000;
		var half = len / 2;
		var array = [];
		var last = new Pe();
		while(len--) {
			array.push(new Pe());
		}
	array.push(last);

	(function(){
		var d = new Date().getTime();
		var i = array.indexOf(last);
		console.log('(indexOf)  Index: ' + i + '\tmilliseconds: ' + (new Date().getTime() - d));
	})();

	(function(){
		var d = new Date().getTime();
		var index = -1;
		for(var i = 0, len = array.length; i < len; i++) {
			if(array[i] === last) {
				index = i;
				break;
			}
		}
		console.log('(for loop) Index: ' + index + '\tmilliseconds: ' + (new Date().getTime() - d));
	})();

	// <!-- JS 產生字串 -->
	var person = {
		name: 'Wes',
		job: 'Web Developer',
		city: 'Hamilton',
		bio: 'Wes is a really cool guy that loves to teach web development!'
	}
	var markups = `
	 <div class="person">
	    <h2>
	        ${person.name}
	    </h2>
	    <p class="location">${person.location}</p>
	    <p class="bio">${person.bio}</p>
	 </div>
	` + `<p>65456456456465465456456</p>`;

	document.body.innerHTML = markups;




	//YT轉RWD

/*	<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container table, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'>

</div>*/



</script>
