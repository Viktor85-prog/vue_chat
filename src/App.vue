<template>
  <div id="app" class="container">
	<div class="chat">
		<div class="chat__header">
			<div class="chat__avatar">
				<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 50 50"><path d="M21.645 11.713c-1.054-1.67 7.832-3.057 8.422 2.054.232 1.54.232 3.107 0 4.647 0 0 1.328-.152.442 2.372 0 0-.488 1.816-1.238 1.408 0 0 .122 2.296-1.058 2.685 0 0 .084 1.223.084 1.306l.986.147s-.03 1.02.167 1.13c.9.58 1.886 1.021 2.923 1.305 3.062.777 4.616 2.11 4.616 3.278l.823 4.189c-3.544 1.485-7.657 2.373-12.055 2.466H24.22c-4.389-.093-8.493-.977-12.03-2.456.161-1.159.371-2.47.588-3.315.466-1.816 3.087-3.165 5.498-4.202 1.248-.537 1.518-.86 2.774-1.409.07-.334.098-.676.084-1.017l1.068-.127s.14.255-.085-1.245c0 0-1.2-.311-1.256-2.7 0 0-.902.3-.956-1.147-.039-.98-.808-1.832.299-2.537l-.564-1.502s-.592-5.8 2.005-5.33z" fill="#FFF" fill-rule="evenodd"/></svg>
			</div>
			<div class="chat__inner">
				<div class="chat__title">
					<div class="chat__bitrixName">Битрикс24</div>
					<div class="chat__time">16 января, 09:23</div>
					<div class="chat__action">Добавлен новый сотрудник</div>
				</div>
				<div class="inner">
					<span class="inner__avatar"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 50 50"><path d="M21.645 11.713c-1.054-1.67 7.832-3.057 8.422 2.054.232 1.54.232 3.107 0 4.647 0 0 1.328-.152.442 2.372 0 0-.488 1.816-1.238 1.408 0 0 .122 2.296-1.058 2.685 0 0 .084 1.223.084 1.306l.986.147s-.03 1.02.167 1.13c.9.58 1.886 1.021 2.923 1.305 3.062.777 4.616 2.11 4.616 3.278l.823 4.189c-3.544 1.485-7.657 2.373-12.055 2.466H24.22c-4.389-.093-8.493-.977-12.03-2.456.161-1.159.371-2.47.588-3.315.466-1.816 3.087-3.165 5.498-4.202 1.248-.537 1.518-.86 2.774-1.409.07-.334.098-.676.084-1.017l1.068-.127s.14.255-.085-1.245c0 0-1.2-.311-1.256-2.7 0 0-.902.3-.956-1.147-.039-.98-.808-1.832.299-2.537l-.564-1.502s-.592-5.8 2.005-5.33z" fill="#FFF" fill-rule="evenodd"/></svg></span>
					<span class="inner__userName">tifani alan</span>
					<span class="inner__importantIcon"></span>
				</div>
				<div class="informers">
					<span>Нравится</span>
					<span>Комментировать</span>
					<span>Не следить</span>
					<span>Ещё</span>
					<span>2</span>
				</div>
				<div class="comments">
					<div class="comments__comment" v-for="(comment) in comments" :key="comment.id">
						<div class="comments__avatar"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 50 50"><path d="M21.645 11.713c-1.054-1.67 7.832-3.057 8.422 2.054.232 1.54.232 3.107 0 4.647 0 0 1.328-.152.442 2.372 0 0-.488 1.816-1.238 1.408 0 0 .122 2.296-1.058 2.685 0 0 .084 1.223.084 1.306l.986.147s-.03 1.02.167 1.13c.9.58 1.886 1.021 2.923 1.305 3.062.777 4.616 2.11 4.616 3.278l.823 4.189c-3.544 1.485-7.657 2.373-12.055 2.466H24.22c-4.389-.093-8.493-.977-12.03-2.456.161-1.159.371-2.47.588-3.315.466-1.816 3.087-3.165 5.498-4.202 1.248-.537 1.518-.86 2.774-1.409.07-.334.098-.676.084-1.017l1.068-.127s.14.255-.085-1.245c0 0-1.2-.311-1.256-2.7 0 0-.902.3-.956-1.147-.039-.98-.808-1.832.299-2.537l-.564-1.502s-.592-5.8 2.005-5.33z" fill="#FFF" fill-rule="evenodd"/></svg></div>
						<div class="comments__inner">
							<div class="comments__content">
								<span class="comments__authorName">
									{{comment.authorName}}
								</span>
								<span class="comments__time">{{comment.time}}</span>
								<div class="comments__text">
									<span class="comments__commentTo">{{comment.commentTo? comment.commentTo + ',' : ''}}</span>
									{{comment.text}}
								</div>
							</div>
							<div class="comments__informers">
								<span>Нравится</span>
								<span>Ответить</span>
								<span>Ещё</span>
							</div>
						</div>
					</div>
					<div class="comments__addComment">
						<div class="comments__avatar"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 50 50"><path d="M21.645 11.713c-1.054-1.67 7.832-3.057 8.422 2.054.232 1.54.232 3.107 0 4.647 0 0 1.328-.152.442 2.372 0 0-.488 1.816-1.238 1.408 0 0 .122 2.296-1.058 2.685 0 0 .084 1.223.084 1.306l.986.147s-.03 1.02.167 1.13c.9.58 1.886 1.021 2.923 1.305 3.062.777 4.616 2.11 4.616 3.278l.823 4.189c-3.544 1.485-7.657 2.373-12.055 2.466H24.22c-4.389-.093-8.493-.977-12.03-2.456.161-1.159.371-2.47.588-3.315.466-1.816 3.087-3.165 5.498-4.202 1.248-.537 1.518-.86 2.774-1.409.07-.334.098-.676.084-1.017l1.068-.127s.14.255-.085-1.245c0 0-1.2-.311-1.256-2.7 0 0-.902.3-.956-1.147-.039-.98-.808-1.832.299-2.537l-.564-1.502s-.592-5.8 2.005-5.33z" fill="#FFF" fill-rule="evenodd"/></svg></div>
						<input class="comments__input" placeholder="Добавить комментарий"/>
					</div>
				</div>
			</div>
		</div>
		<Message/>
	</div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
	return {
		comments: [{
			id: 1,
			authorName: 'tifani alan',
			time: '12:36',
			text: 'sasasas',
			commentTo: ''
		},{
			id:2,
			authorName: 'tifani alan',
			time: '12:36',
			text: 'asasa',
			commentTo: ''
		},{
			id:3,
			authorName: 'tifani alan',
			time: '12:36',
			text: 'sasasa',
			commentTo: 'tifani alan'
		}]
	}
  }
}
</script>

<style>
body {
	margin: 0;
	color: #7f7f7f;
    font-size: 14px;
    line-height: 16px;
	font-family: 'Open Sans','Helvetica Neue',Helvetica,Arial,sans-serif;
}

.container {
	min-width: 1080px;
	min-height: 500px;
	padding: 20px;
	background-color: #2958B4;
}

.chat {
	width: 800px;
	min-height: 350px;
	padding: 10px;
	background-color: #fff;
	border-radius: 5px;
}

.chat__header {
	margin-bottom: 2px;
    padding: 18px;
	display: flex;
}

.chat__avatar {
	background-color: #7b8691;
	width: 50px;
    height: 50px;
    border-radius: 50%;
    display: block;
    /* float: left; */
    margin-right: 17px;
    overflow: hidden;
	
}
.chat__bitrixName {
	border-bottom: 1px solid transparent;
    color: #2067b0;
    display: inline-block;
    font-size: 14px;
    font-weight: 600;
    margin: 0 4px 0 0;
    vertical-align: middle;
}

.chat__time {
	padding-top: 3px;
}

.chat__action{
	color: #5c6470;
    font-size: 12px;
    margin: 0;
    overflow: hidden;
    padding: 12px 0 1px;
    vertical-align: top;
}

.inner {
	min-height: 85px;
    max-height: 285px;
    max-width: 867px;
    min-width: 500px;
	padding: 9px 15px;
    overflow: hidden;
    word-wrap: break-word;
	font-size: 14.5px;
	background-color: #f3fed6;
	background-position: top right;
    background-repeat: no-repeat;
	background-image: url("data:image/svg+xml;charset=utf-8,%3Csvg width='317' height='358' fill='none' xmlns='http://www.w3.org/2000/svg'%3E%3Cmask id='a' maskUnits='userSpaceOnUse' x='0' y='0' width='317' height='358'%3E%3Cpath fill-rule='evenodd' clip-rule='evenodd' d='M0 0h317v358H0V0z' fill='%23F3FED6'/%3E%3C/mask%3E%3Cg mask='url(%23a)' fill-rule='evenodd' clip-rule='evenodd'%3E%3Cpath d='M-550 .17h867v358h-867V.17z' fill='%23F3FED6'/%3E%3Cpath opacity='.1' d='M329 182.5c0 83.119-67.381 150.5-150.5 150.5S28 265.619 28 182.5 95.381 32 178.5 32 329 99.381 329 182.5zm-32.765 0c0 65.023-52.712 117.735-117.735 117.735S60.765 247.523 60.765 182.5 113.477 64.765 178.5 64.765 296.235 117.477 296.235 182.5zm-99.477-17.117h-31.976v.007h-13.719v13.072h13.719v71.709h-13.719v13.718h54.874v-13.718h-9.179v-84.788zm6.279-42.224c0 12.689-10.286 22.975-22.974 22.975s-22.974-10.286-22.974-22.975c0-12.688 10.286-22.974 22.974-22.974s22.974 10.286 22.974 22.974z' fill='%239DCF00'/%3E%3C/g%3E%3C/svg%3E");
    border-radius: 23px;
    margin: 12px 0 0;
}

.inner__avatar {
	display: inline-block;
    float: none;
    margin-right: 10px;
    position: static;
    vertical-align: middle;
	width: 50px;
    height: 50px;
    border-radius: 50%;
	background-color: #2958B4;
}

.inner__userName{
	width: auto;
	line-height: 16px;
	vertical-align: middle;
	color: #0b66c3;
    font-weight: bold;
    max-width: 100%;
}

.inner__importantIcon {
	width: 56px;
    height: 56px;
	float: right;
	border-radius: 50%;
	margin: 23px 32px;
	background-image: url("data:image/svg+xml;charset=utf-8,%3Csvg width='57' height='57' fill='none' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath fill-rule='evenodd' clip-rule='evenodd' d='M29.613 56.473a27.997 27.997 0 1126.882-27.977c.294 15.146-11.737 27.667-26.882 27.977z' fill='%23fff'/%3E%3Cpath fill-rule='evenodd' clip-rule='evenodd' d='M28.503 48.5c11.045 0 20-8.954 20-20s-8.955-20-20-20c-11.046 0-20 8.954-20 20s8.954 20 20 20zm.23-25.353a3.382 3.382 0 100-6.764 3.382 3.382 0 000 6.764zm2.457 2.833h-4.707v.001h-2.02v1.924h2.02v10.556h-2.02v2.02h8.078v-2.02h-1.35v-12.48z' fill='%239DCF00'/%3E%3C/svg%3E")
}

.informers {
	padding-top: 18px;
	min-height: 25px;
	font-size: 13px;
    line-height: 13px;
	text-align: left;
}

.informers span {
	margin-right: 13px;
}

.comments {
	border-radius: 1px;
    margin: 4px 0;
    position: relative;
}

.comments__comment {
	margin-bottom: 10px;
    margin-top: 1px;
	display: flex;
    min-height: 40px;
    max-width: calc(100% - 60px);
}

.comments__avatar {
	width: 37px;
    height: 37px;
	margin-right: 10px;
    border-radius: 50%;
	background-color: #7b8691;
}

.comments__content {
	/* position: relative; */
    padding: 7px 21px 7px 15px;
    max-width: 820px;
    border-radius: 23px;
    background-color: #edf1f3;
    box-sizing: border-box;
    overflow: hidden;
}
.comments__inner {
	margin-bottom: 10px;
}
.comments__authorName {
	margin-bottom: 1px;
    line-height: 16px;
	font-size: 13px;
	font-weight: bold;
	margin-right: 7px;
	color: #2067b0;
}

.comments__time {
    color: #bcc2c7;
    font-size: 11px;
}

.comments__text {
	font-size: 13px;
	max-height: 200px;
    overflow: hidden;
	color: #151515;
}

.comments__informers span{
	color: #a8aeb5;
	font-size: 12px;
    line-height: 12px;
	margin: 8px 10px;
}

.comments__commentTo {
	color: #2067b0;
}

.comments__addComment {
	padding-top: 3px;
	display: flex;
}

.comments__input {
	height: 39px;
	width: 90%;
	border-radius: 40px;
	border-color: #a8adb4;;
    cursor: pointer;
	color: #a8adb4;
	padding: 0 15px;
    vertical-align: top;
    font-size: 13px;
}
</style>
