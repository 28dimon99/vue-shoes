<template>
    <div>
        <v-app class="side_bar">
            <SideBar :drawer="drawer"/>
            <RightSideBar/>
            <v-container>
                <v-toolbar flat color="transparent">
                    <v-btn icon dark class="d-lg-none d-xl-flex" @click.stop="drawer = !drawer">
                        <v-icon>mdi-menu</v-icon>
                    </v-btn>
                    <v-spacer></v-spacer>
                    <v-text-field
                            label="Search on maufarm"
                            class="pt-5 d-none d-sm-flex"
                            dark filled prepend-inner-icon="mdi-magnify"
                            solo flat
                            background-color="transparent"
                            rounded outlined
                    >

                    </v-text-field>
                    <v-spacer></v-spacer>
                    <v-btn dark class="mr-2">
                        <v-icon left>fas fa-filter</v-icon>
                        Filter
                    </v-btn>
                    <v-btn dark class="mr-2">
                        <v-icon left>fas fa-upload</v-icon>
                        Export
                    </v-btn>
                </v-toolbar>
                <h1 class="white--text">SALES</h1>
                <p class="grey--text">
                    A Great Way To Generate All The Motivation You Need To Get Fit
                </p>
                <v-app-bar dark color="transparent" flat>
                    <v-tabs color="#6F0DFF">
                        <v-tabs-slider color="#6F0DFF"></v-tabs-slider>
                        <v-tab class="withoutupercase">Fultillment Status Views</v-tab>
                        <v-tab class="withoutupercase">Real-time Tracking</v-tab>
                        <v-tab class="withoutupercase">Sales View</v-tab>
                        <v-tab class="withoutupercase">Balances</v-tab>
                        <v-tab class="withoutupercase">Transactions</v-tab>
                        <v-tab class="withoutupercase">Engagement Rate</v-tab>
                    </v-tabs>
                    <v-spacer></v-spacer>
                    <v-btn dark text class="d-none d-sm-flex">
                        <v-icon left>mdi-magnify</v-icon>
                        SEARCH
                    </v-btn>
                    <v-btn rounded color="white" class="black--text">
                        LIST
                        <v-icon right>mdi-format-list-bulleted</v-icon>
                    </v-btn>
                    <v-btn icon>
                        <v-icon>mdi-apps</v-icon>
                    </v-btn>
                </v-app-bar>
                <v-toolbar flat color="transparent">
                    <v-divider vertical color="green" inset></v-divider>
                    <v-toolbar-title class="white--text ml-4">Alert</v-toolbar-title>
                    <v-spacer></v-spacer>
                    <v-chip class="ma-1 d-none d-sm-flex" label text-color="white" dark>
                        <v-avatar color="white" rounded class="mr-2">
                            <v-img src="https://static.wixstatic.com/media/82fcd3_5f43b28d86784d2fadef962d65b2c781~mv2_d_1920_1920_s_2.jpg/v1/fill/w_256,h_256,al_c,q_80,usm_0.66_1.00_0.01/82fcd3_5f43b28d86784d2fadef962d65b2c781~mv2_d_1920_1920_s_2.webp">
                            </v-img>
                        </v-avatar>
                        Nike new golf
                    </v-chip>
                    <v-chip class="ma-1 d-none d-sm-flex" label text-color="white" dark>
                        <v-avatar color="white" rounded class="mr-2">
                            <v-img src="https://static.wixstatic.com/media/82fcd3_187d47b7648241cdb412ae9ec1491601~mv2_d_1920_1920_s_2.jpg/v1/fill/w_256,h_256,al_c,q_80,usm_0.66_1.00_0.01/82fcd3_187d47b7648241cdb412ae9ec1491601~mv2_d_1920_1920_s_2.webp">
                            </v-img>
                        </v-avatar>
                        Sneakers printemps
                    </v-chip>
                    <v-spacer></v-spacer>
                    <v-btn dark class="mr-2 withoutupercase d-none d-sm-flex">See All (10)</v-btn>
                    <v-btn dark class="mr-2" outlined>
                        <v-icon left>mdi-chevron-left</v-icon>
                        <v-icon left>mdi-chevron-right</v-icon>
                    </v-btn>
                </v-toolbar>
                <v-row class="mt-n14">
                    <v-col cols="12" xs="12" sm="6" md="4" lg="3" v-for="(shoe, i) in shoes" :key="i">
                        <v-card class="mx-auto mt-12 rounded-xl" max-width="374" color="#151515">
                            <v-img height="170" :src="shoe.image"></v-img>
                            <v-toolbar color="transparent" class="mt-n7" flat>
                                <v-avatar color="white" rounded class="mr-2">
                                    <v-img :src="shoe.image" contain></v-img>
                                </v-avatar>
                                <v-spacer></v-spacer>
                                <v-avatar color="black" rounded class="mr-2" dark>
                                    <div class="three">
                                        <div class="four">
                                            <span class="white--text caption">{{shoe.price}}$</span>
                                        </div>
                                        <div class="five"><span class="green--text caption">HOLD</span></div>
                                    </div>
                                </v-avatar>
                            </v-toolbar>
                            <v-card-title class="grey--text caption">{{shoe.id}}</v-card-title>
                            <v-card-title class="grey--text text-grey-darken-1 caption mt-n6">{{shoe.name}}
                            </v-card-title>
                            <v-card-text class="white--text text-grey-darken-1 mt-n2">{{shoe.model}}</v-card-text>
                            <v-card-text class="mt-n4">
                                <v-chip-group active-class="deep-purple accent-4 white--text" column>
                                    <v-chip label dark>{{shoe.pay1}}</v-chip>
                                    <v-chip label dark>{{shoe.pay2}}</v-chip>
                                    <v-spacer></v-spacer>
                                    <v-avatar size="40">
                                        <v-img></v-img>
                                    </v-avatar>
                                </v-chip-group>
                            </v-card-text>
                        </v-card>
                    </v-col>
                </v-row>


                <v-toolbar flat color="transparent" class="mt-12">
                    <v-divider vertical color="orange" inset></v-divider>
                    <v-toolbar-title class="white--text ml-4">Recent Orders</v-toolbar-title>
                    <v-spacer></v-spacer>
                    <v-chip class="ma-1 d-none d-sm-flex" label text-color="white" dark>
                        <v-avatar color="white" rounded class="mr-2">
                            <v-img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ2rMGRS3YV5x8iRJkLYKtkjevs1F45XqFcBw&usqp=CAU"
                                   contain></v-img>
                        </v-avatar>
                        Nike new
                    </v-chip>
                    <v-chip class="ma-1 d-none d-sm-flex" label text-color="white" dark>
                        <v-avatar color="white" rounded class="mr-2">
                            <v-img src="https://static.wixstatic.com/media/82fcd3_00e03bcc284741fd839c3578729099d0~mv2_d_1920_1920_s_2.jpg/v1/fill/w_256,h_256,al_c,q_80,usm_0.66_1.00_0.01/82fcd3_00e03bcc284741fd839c3578729099d0~mv2_d_1920_1920_s_2.webp"
                                   contain></v-img>
                        </v-avatar>
                        Zoom Jo
                    </v-chip>
                    <v-chip class="ma-1 d-none d-sm-flex" label text-color="white" dark>
                        <v-avatar color="white" rounded class="mr-2">
                            <v-img src="https://static.wixstatic.com/media/82fcd3_5f43b28d86784d2fadef962d65b2c781~mv2_d_1920_1920_s_2.jpg/v1/fill/w_256,h_256,al_c,q_80,usm_0.66_1.00_0.01/82fcd3_5f43b28d86784d2fadef962d65b2c781~mv2_d_1920_1920_s_2.webp"
                                   contain></v-img>
                        </v-avatar>
                        Jordon BZ
                    </v-chip>
                    <v-spacer></v-spacer>
                    <v-btn dark class="mr-2 withoutupercase d-none s-sm-flex">
                        See All (129)
                    </v-btn>
                    <v-btn dark class="mr-2" outlined>
                        <v-icon left>mdi-chevron-left</v-icon>
                        <v-icon right>mdi-chevron-right</v-icon>
                    </v-btn>
                </v-toolbar>
                <v-row class="mt-10">
                    <v-col cols="12" xs="12" sm="6" md="3" v-for="(order, i) in orders" :key="i">
                        <v-card class="mx-auto my-12 rounded-lg" max-width="374" color="#151515">
                            <v-toolbar color="transparent" class="mt-n6" flat>
                                <v-avatar color="white" rounded class="mr-2">
                                    <v-img :src="order.pic"></v-img>
                                </v-avatar>
                                <v-spacer></v-spacer>
                                <v-avatar color="black" rounded class="mr-2" dark>
                                    <div class="three">
                                        <div class="four">
                                            <span class="white--text caption">{{order.price}}</span>
                                        </div>
                                        <div class="six">
                                            <span class="orange--text caption">HOLD</span>
                                        </div>
                                    </div>
                                </v-avatar>
                            </v-toolbar>
                        </v-card>
                    </v-col>
                </v-row>

            </v-container>
        </v-app>
    </div>

</template>

<script>


    import SideBar from "../components/SideBar";
    import RightSideBar from "../components/RightSideBar";


    export default {
        name: 'Home',
        components: {
            SideBar, RightSideBar,
        },
        data() {
            return {
                selection: 1,
                drawer: true,
                shoes: [
                    {
                        "id": 0,
                        "name": "Tent",
                        "model": "T-123",
                        "image": "https://static.wixstatic.com/media/82fcd3_5f43b28d86784d2fadef962d65b2c781~mv2_d_1920_1920_s_2.jpg/v1/fill/w_256,h_256,al_c,q_80,usm_0.66_1.00_0.01/82fcd3_5f43b28d86784d2fadef962d65b2c781~mv2_d_1920_1920_s_2.webp",
                        "price": 102,
                        "pay1": 111,
                        "pay2": 222,

                    },
                    {
                        "id": 1,
                        "name": "Tent",
                        "model": "T-336",
                        "image": "https://static.wixstatic.com/media/82fcd3_00e03bcc284741fd839c3578729099d0~mv2_d_1920_1920_s_2.jpg/v1/fill/w_256,h_256,al_c,q_80,usm_0.66_1.00_0.01/82fcd3_00e03bcc284741fd839c3578729099d0~mv2_d_1920_1920_s_2.webp",
                        "price": 106,
                        "pay1": 333,
                        "pay2": 444,
                    },
                    {
                        "id": 2,
                        "name": "Tent",
                        "model": "T-456",
                        "image": "https://static.wixstatic.com/media/82fcd3_187d47b7648241cdb412ae9ec1491601~mv2_d_1920_1920_s_2.jpg/v1/fill/w_256,h_256,al_c,q_80,usm_0.66_1.00_0.01/82fcd3_187d47b7648241cdb412ae9ec1491601~mv2_d_1920_1920_s_2.webp",
                        "price": 115,
                        "pay1": 555,
                        "pay2": 666,
                    },
                    {
                        "id": 3,
                        "name": "Tent",
                        "model": "T-123",
                        "image": "https://static.wixstatic.com/media/82fcd3_5f43b28d86784d2fadef962d65b2c781~mv2_d_1920_1920_s_2.jpg/v1/fill/w_256,h_256,al_c,q_80,usm_0.66_1.00_0.01/82fcd3_5f43b28d86784d2fadef962d65b2c781~mv2_d_1920_1920_s_2.webp",
                        "price": 102,
                        "pay1": 777,
                        "pay2": 888,
                    },
                    {
                        "id": 4,
                        "name": "Tent",
                        "model": "T-336",
                        "image": "https://static.wixstatic.com/media/82fcd3_00e03bcc284741fd839c3578729099d0~mv2_d_1920_1920_s_2.jpg/v1/fill/w_256,h_256,al_c,q_80,usm_0.66_1.00_0.01/82fcd3_00e03bcc284741fd839c3578729099d0~mv2_d_1920_1920_s_2.webp",
                        "price": 106,
                        "pay1": 999,
                        "pay2": 1000,
                    },
                    {
                        "id": 5,
                        "name": "Tent",
                        "model": "T-456",
                        "image": "https://static.wixstatic.com/media/82fcd3_187d47b7648241cdb412ae9ec1491601~mv2_d_1920_1920_s_2.jpg/v1/fill/w_256,h_256,al_c,q_80,usm_0.66_1.00_0.01/82fcd3_187d47b7648241cdb412ae9ec1491601~mv2_d_1920_1920_s_2.webp",
                        "price": 115,
                        "pay1": 1100,
                        "pay2": 1200,
                    },
                    {
                        "id": 6,
                        "name": "Tent",
                        "model": "T-123",
                        "image": "https://static.wixstatic.com/media/82fcd3_5f43b28d86784d2fadef962d65b2c781~mv2_d_1920_1920_s_2.jpg/v1/fill/w_256,h_256,al_c,q_80,usm_0.66_1.00_0.01/82fcd3_5f43b28d86784d2fadef962d65b2c781~mv2_d_1920_1920_s_2.webp",
                        "price": 102,
                        "pay1": 1300,
                        "pay2": 1400,
                    },
                    {
                        "id": 7,
                        "name": "Tent",
                        "model": "T-336",
                        "image": "https://static.wixstatic.com/media/82fcd3_00e03bcc284741fd839c3578729099d0~mv2_d_1920_1920_s_2.jpg/v1/fill/w_256,h_256,al_c,q_80,usm_0.66_1.00_0.01/82fcd3_00e03bcc284741fd839c3578729099d0~mv2_d_1920_1920_s_2.webp",
                        "price": 106,
                        "pay1": 1500,
                        "pay2": 1600,
                    },

                ],
                orders: [
                    {
                        pic: "data:image/jpeg;base64,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",
                        price: "$465"
                    },
                    {
                        pic: "data:image/jpeg;base64,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",
                        price: "$714"
                    },
                    {
                        pic: "data:image/jpeg;base64,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",
                        price: "$982"
                    },
                    {
                        pic: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ2rMGRS3YV5x8iRJkLYKtkjevs1F45XqFcBw&usqp=CAU",
                        price: "$394"
                    }
                ]
            }
        }
    }
</script>
<style scoped lang="scss">
    .side_bar {
        background: #000000;
    }

    .v-tab.withoutupercase {
        text-transform: none !important;
    }

    .v-tabs {
        width: 50% !important;
    }

    .v-btn.withoutupercase {
        text-transform: none !important;
    }

    .three {
        width: 50px;
        height: 50px;
    }

    .four {
        width: 50px;
        height: 25px;
        background: black;
    }

    .five {
        width: 50px;
        height: 25px;
        background: #042aof;
    }
</style>
