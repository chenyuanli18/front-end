    <template>  
        <view>  
			<van-search
			  value=""
			  placeholder="搜索专业/学校/机构"
			  show-action
			  bind:search="onSearch"
			  bind:cancel="onCancel"
			/>
			
			<van-tabs active="active" bind:change="onChange">
			  <van-tab title="全部"></van-tab>
			  <van-tab title="我关注的"></van-tab>
			  <van-tab title="学校"></van-tab>
			</van-tabs>
			
			<van-cell-group>
			  <van-cell title="波士顿大学" value="自主" size="large" label="MS Bioinformatics" />
			</van-cell-group>
			<van-cell-group>
			  <van-cell title="弗吉尼亚大学" value="自主" size="large" label="MS MCS" />
			</van-cell-group>
			<van-cell-group>
			  <van-cell title="加州大学圣克鲁兹分校" value="机构" size="large" label="MS CSE" />
			</van-cell-group>
			<van-cell-group>
			  <van-cell title="东北大学" value="自主" size="large" label="MS Game Science and Design" />
			</van-cell-group>
			<van-cell-group>
			  <van-cell title="纽约大学" value="自主" size="large" label="MS Courant" />
			</van-cell-group>
			<van-cell-group>
			  <van-cell title="帝国理工大学" value="机构" size="large" label="MS Computing(visual computing)" />
			</van-cell-group>
			<van-cell-group>
			  <van-cell title="约翰霍普金斯大学" value="自主" size="large" label="MS Biomedical Engineering" />
			</van-cell-group>
			<van-cell-group>
			  <van-cell title="已经没有可以看的内容" value="" size="large"/>
			</van-cell-group>
			
			<van-tabbar active="active" bind:change="onChange">
			  <van-tabbar-item icon="home-o">标签</van-tabbar-item>
			  <van-tabbar-item icon="search">标签</van-tabbar-item>
			  <van-tabbar-item icon="friends-o">标签</van-tabbar-item>
			  <van-tabbar-item icon="setting-o">标签</van-tabbar-item>
			</van-tabbar>
			
        </view>  
    </template>  
	
    <script>  
        export default {
        	data() {  
        		return {  
        			value:"123",  
        			buttontype:"primary",
					active: 1,
        			}; 	
        },
		onChange(event) {
		    wx.showToast({
		      title: `切换到标签 ${event.detail.name}`,
		      icon: 'none',
		    })
		  },
         }
    </script> 
	 
    <style>
		
    </style>