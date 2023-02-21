<template>
  <div id="app" class="container">
	<div class="chat">
		<div class="chat__header">
			<div class="chat__avatar">
			</div>
			<div class="chat__inner">
				<div class="chat__title">
					<div class="chat__bitrixName">Битрикс24</div>
					<div class="chat__time">16 января, 09:23</div>
					<div class="chat__action">Добавлен новый сотрудник</div>
				</div>
				<div class="inner">
					<span class="inner__avatar"></span>
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
					<div class="comments__comment">
						<div class="comments__avatar"></div>
						<div class="">
							<div class="comments__content">
								<span class="comments__authorName">
									tifani alan
								</span>
								<span class="comments__time">12:36</span>
								<div class="comments__text">sasasa</div>
							</div>
							<div class="comments__informers">
								<span>Нравится</span>
								<span>Ответить</span>
								<span>Ещё</span>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
		<Message/>
	</div>
  </div>
</template>

<script>
import Message from './components/Message.vue'

export default {
  name: 'App',
  components: {
    Message
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
	height: 500px;
	padding: 20px;
	background-color: #2958B4;
}

.chat {
	width: 800px;
	height: 350px;
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
	background-color: red;
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
	/* background-position: top right; */
    /* background-repeat: no-repeat; */
    border-radius: 23px;
    margin: 12px 0 0;
}

.dv {
	background: url('https://b24-m9zo2s.bitrix24.ru/b24237232/resize_cache/127/7acf4cadf975128573a8b1c2766af5d8/main/260/260b25a0528fb6185ef5d15adf261290/d7f065ee880772c5d6464e8965a4e8d2.jpg');
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
	background-color: red;
	border-radius: 50%;
	margin: 23px 32px;
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
    border-radius: 50%;
	background-color: red;
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
</style>
