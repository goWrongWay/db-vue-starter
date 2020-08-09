<style scoped>
    .layout {
        min-height: 100vh;
        background: #f5f7f9;
        overflow: hidden;
    }

    .layout-logo {
        height: 65px;
        line-height: 66px;
        border-bottom: 1px solid #f3f2f2;
        border-right: 1px solid rgba(243, 242, 242, 0.76);
        font-size: 18px;
        color: #333;
    }

    .ivu-layout-sider {
        height: 100vh;
    }

    .ivu-layout-sider, .ivu-layout-header {
        background: #fff;
    }

    .ivu-menu {
        height: 100%;
    }
    .ivu-layout-content {
        padding: 10px;
    }

</style>
<template>
    <div class="layout">
        <Layout>
            <Sider>
                <Header class="layout-logo">全速-供应链</Header>
                <Menu :active-name="pathname" width="auto">
                    <MenuItem name="/" to="/">
                        <Icon type="ios-navigate"></Icon>
                        <span>Option 1</span>
                    </MenuItem>
                    <MenuItem name="/about" to="/about">
                        <Icon type="ios-search"></Icon>
                        <span>Option 2</span>
                    </MenuItem>
                    <MenuItem name="/route66" to="/route66">
                        <Icon type="ios-settings"></Icon>
                        <span>Option 3</span>
                    </MenuItem>
                    <MenuItem name="/lightbulb" to="/lightbulb">
                        <Icon type="ios-settings"></Icon>
                        <span>Option 4</span>
                    </MenuItem>
                </Menu>
                <div slot="trigger"></div>
            </Sider>
            <Layout>
                <Header class="layout-header-bar"></Header>
                <Content :style="{margin: '20px', background: '#fff', minHeight: '220px'}">
                    <router-view></router-view>
                </Content>
            </Layout>
        </Layout>
    </div>
</template>
<script>
    export default {
        data: () => (
            {
                pathname: window.location.pathname,
            }
        ),
        created() {
            console.log(this.pathname);
        }
    }
</script>