<template>
    <main>
        <div class="wrap">
            <div class="block-wrap">
                <div class="block">
                    <a href="#">
                        <img 
                            v-for="image in images"
                            :key="image.id"
                            :src="image.image"
                        >
                    </a>
                </div><!--block-->
                <div class="block">
                    <a href="#">
                        <img 
                            v-for="image1 in images1"
                            :key="image1.id"
                            :src="image1.image"
                        >
                    </a>
                </div><!--block-->
            </div><!--/.block-wrap-->
            <div class="member-spotlight">
                <div class="member">
                    <img src="../assets/images/member.png">
                    <p>LOOKMEはオンラインサロンの支援金によって支えられています。ご支援いただくと、LOOKMEの活動報告が毎日投稿される、非公開のFacebookグループにご招待。支援金は、LOOKMEのサイト運営や各種企画の実施に使わせていただきます。</p>
                    <a href="#"><img src="../assets/images/details.png"></a>
                </div><!--member-->
                <div class="spotlight">
                    <img src="../assets/images/spotlight.png">
                    <p>LOOKME（ルックミー）は、「<span>革新的なサービスを生み出していたり、ユニークな活動をしている人</span>」と「<span>メディア運営をしている人</span>（<span>ライターやエディター</span>）」をつなぐ取材マッチングサービスです。SNSでの発信力のある人についつい目がいきがち・・ですが、魅力的な人はまだまだいる。そんな「実は」すごい人にスポットライトがあたる、出会いの場を提供します。</p>
                    <p>報酬や規模ではなく、『共感』で「取材したい」人と「取材されてもいいよ！」って人が出会うことが出来ます。</p>
                </div><!--spotlight-->
            </div><!--/.member-spotlight-->
        </div><!--/.wrap-->
        <div class="how">
            <img class="image" src="../assets/images/how.png">
            <ul class="tab_list">
                <li @click="change('A')" :class="{'active':isActive === 'A'}">
                    <img class="smart" src="../assets/images/coveraged1.png">
                    <img class="pc" src="../assets/images/how_tab_me.png">
                </li>
                <li @click="change('B')" :class="{'active':isActive === 'B'}">
                    <img class="smart" src="../assets/images/coverage1.png">
                    <img class="pc" src="../assets/images/how_tab_you.png">
                </li>
            </ul>
            <div 
                class="content"
                v-if="isActive === 'A'"  
            >
                <div class="content-wrap">
                    <div>
                        <img src="../assets/images/coveraged-step1.png">
                        <p>Twitterアカウントでかんたんに登録完了！無料でサービスの利用を開始できます。</p>
                    </div>
                    <img src="../assets/images/subscribe1.png">
                </div><!--/.content-wrap-->
                <div class="content-wrap">
                    <div>
                        <img src="../assets/images/coveraged-step2.png">
                        <p>あなたのプロフィールや活動内容を登録して、取材したい人からのオファーを待ちましょう。</p>
                    </div>
                    <img src="../assets/images/me.png">
                </div><!--/.content-wrap-->
                <div class="content-wrap">
                    <div>
                        <img src="../assets/images/coveraged-step3.png">
                        <p>あなたを取材したい人からTwitter経由でDMが届きます。取材に応じてあなたのことをたくさんの人に知ってもらいましょう。</p>
                    </div>
                    <img src="../assets/images/matching.png">
                </div><!--/.content-wrap-->
                <img class="coveraged" src="../assets/images/cta_ttl_me.png">
                <a href="#"><img class="subscribe" src="../assets/images/subscribe.png"></a>
            </div><!--/.content-->
            <div 
                class="article"
                v-else-if="isActive === 'B'"  
            >
                <div class="content-wrap">
                    <div>
                        <img src="../assets/images/how_you_step01.png">
                        <p>LOOKMEのユーザーは全員取材OK!会って会員登録なしで気になる人を探せます。</p>
                    </div>
                    <img class="step1" src="../assets/images/how_you_img01.png">
                </div><!--/.content-wrap-->
                <div class="content-wrap">
                    <div>
                        <img src="../assets/images/how_you_step02.png">
                        <p>プロフィールを見て取材したい！と思ったらぜひTwitterでDMを送ってみましょう。</p>
                    </div>
                    <img src="../assets/images/me.png">
                </div><!--/.content-wrap-->
                <div class="content-wrap">
                    <div>
                        <img src="../assets/images/coveraged-step3.png">
                        <p>相手からOKがもらえたらマッチング成立！<br>魅力ある人の活動を取材して記事を作りましょう。</p>
                    </div>
                    <img src="../assets/images/matching.png">
                </div><!--/.content-wrap-->
                <img class="coveraged" src="../assets/images/how_tab_you.png">
                <a href="#"><img class="subscribe" src="../assets/images/site.png"></a>
            </div><!--/.articles-wrap-->
            <div class="member-wrap">
                <div class="member">
                    <img src="../assets/images/member.png">
                    <p>LOOKMEはオンラインサロンの支援金によって支えられています。ご支援いただくと、LOOKMEの活動報告が毎日投稿される、非公開のFacebookグループにご招待。支援金は、LOOKMEのサイト運営や各種企画の実施に使わせていただきます。</p>
                    <a href="#"><img src="../assets/images/details.png"></a>
                </div><!--member-->
            </div><!--/.member-wrap-->
        </div><!--/.how-->
        <div class="bottom">
            <div class="bottom-wrap">
                <div>
                    <img class="bottom-image" src="../assets/images/sns_tw_ttl.png">
                    <div class="bottom-block">
                        <img class="bottom-image" src="../assets/images/sns_tw_official.png">
                        <img class="bottom-image" src="../assets/images/sns_tw_lookkun.png">
                        <img class="bottom-image" src="../assets/images/sns_tw_txt.png">
                    </div><!--/.bottom-block-->
                    <a href="#"><img class="bottom-image1" src="../assets/images/sns_tw_btn.png"></a>
                </div>
                <div>
                    <p class="company-name">運営：株式会社ヒトコト</p>
                    <p class="company-address">〒810-0024<br>福岡県福岡市中央区桜坂3丁目4-18</p>
                    <p class="contact"><a href="#">お問い合わせ</a></p>
                </div>
            </div><!--/.bottom-wrap-->
        </div><!--/.bottom-->
    </main>
</template>

<script>
    export default{
        data:function(){
            return{
                images:[
                    {
                        image:require('@/assets/images/coveraged.png')
                    },
                    {
                        image:require('@/assets/images/subscribe.png')
                    }
                ],
                images1:[
                    {
                        image:require('@/assets/images/coverage.png')
                    },
                    {
                        image:require('@/assets/images/site.png')
                    }
                ],
           
                isActive:'A'
            }
        },
        methods:{
            change:function(num){
                this.isActive = num
            }
        }
    }
</script>