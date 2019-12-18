<template>
	<div id="app">
		
		<layout>
			
			<!-- slot은 template으로 바뀜 -->
			<template #header="header">
				<h1>{{header.title}}</h1>
			</template>
			<template #sidebar="sidebar">
				<h3>{{sidebar.title}}</h3>
				<ul class="menu">
					<li v-for="i of sidebars" :key="i.menu">
						<!-- <a :href="i.link">{{i.menu}}</a> -->
						<router-link :to="i.link">{{i.menu}}</router-link>
						
					</li>
				</ul>
			</template>
			<template #content="content">
				<h2>{{content.title}}</h2>
				<router-view/>
			</template>
			<template #footer="footer">
				<h3>{{footer.title}}</h3>
			</template>
		</layout>
	</div>
</template>
<script>
import Layout from "@/components/Layout.vue"
export default{
	components : {
		Layout
	},
	data(){
		return{
			sidebars : [{ menu : "Home", link : '/' }, 
						{ menu : "장바구니", link : '/cart' },
						{ menu : "계산기", link : '/calculator' },
						{ menu : "두 수 합", link : '/seqsum' },
						{ menu : "계좌 개설", link : '/account' },
						{ menu : "할일 목록", link : '/todo' },
						{ menu : "슬롯 테스트", link : '/parent' } ]
		}
	}
}
</script>
<style scoped>
ul.menu {
    position:relative;
    padding: 5px 5px 5px 5px;
    list-style: none;
    font-style: italic;
}
ul.menu a {
    text-decoration:none;
}
</style>