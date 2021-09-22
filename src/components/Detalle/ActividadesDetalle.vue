<template>
    <div>
        <img v-bind:src="JSON.parse(actividad.activity).image[1]" alt="" class="contenedor_detalle--imagen"/>

                <div class="control">
                     <div class="contenedor_principal--titulo">{{actividad.title}}</div>
                    <div class="contenedor_principal--descrip">{{JSON.parse(actividad.activity).description}}</div>
                    <div class="contenedor_principal--subtitle">
                        <svg xmlns="http://www.w3.org/2000/svg" width="14" height="16" viewBox="0 0 14 16" fill="none">
                        <path d="M3.33792 4.66668C3.33792 3.94148 3.543 3.23257 3.92722 2.62959C4.31144 2.02661 4.85755 1.55665 5.49649 1.27912C6.13542 1.0016 6.83849 0.928991 7.51678 1.07047C8.19507 1.21195 8.81812 1.56117 9.30714 2.07396C9.79616 2.58675 10.1292 3.24009 10.2641 3.95135C10.399 4.66262 10.3298 5.39986 10.0651 6.06986C9.80047 6.73985 9.35229 7.31251 8.77727 7.7154C8.20224 8.1183 7.52619 8.33335 6.83461 8.33335C7.58074 8.33531 8.32158 8.46479 9.02799 8.71668C9.88314 8.20875 10.5539 7.41828 10.9356 6.4686C11.3173 5.51892 11.3885 4.46346 11.138 3.4669C10.8875 2.47035 10.3295 1.58876 9.55106 0.959705C8.77258 0.330647 7.81742 -0.010498 6.83461 -0.010498C5.85181 -0.010498 4.89664 0.330647 4.11816 0.959705C3.33968 1.58876 2.78168 2.47035 2.53122 3.4669C2.28076 4.46346 2.35193 5.51892 2.73363 6.4686C3.11533 7.41828 3.78608 8.20875 4.64123 8.71668C5.34764 8.46479 6.08848 8.33531 6.83461 8.33335C5.90723 8.33335 5.01783 7.94704 4.36208 7.25941C3.70632 6.57177 3.33792 5.63914 3.33792 4.66668Z" fill="#464646"/>
                        <path d="M0 15.5001C0 15.6327 0.0502364 15.7599 0.139658 15.8537C0.229079 15.9475 0.35036 16.0001 0.476821 16.0001C0.603282 16.0001 0.724563 15.9475 0.813985 15.8537C0.903406 15.7599 0.953642 15.6327 0.953642 15.5001C0.955745 13.8653 1.576 12.2981 2.67841 11.1421C3.78082 9.98608 5.2754 9.33567 6.83444 9.33346C6.06412 9.33533 5.30717 9.12251 4.64106 8.7168C3.29059 9.20059 2.11768 10.1141 1.28577 11.33C0.453864 12.5459 0.0043954 14.0037 0 15.5001H0Z" fill="#464646"/>
                        <path d="M11.5868 11.3751C11.7139 11.1835 11.8729 11.0085 12.0159 10.8335C11.2157 9.86347 10.1847 9.13313 9.02785 8.7168C8.36174 9.12251 7.60479 9.33533 6.83447 9.33346C8.39351 9.33567 9.88809 9.98608 10.9905 11.1421C12.0929 12.2981 12.7132 13.8653 12.7153 15.5001C12.7153 15.6327 12.7655 15.7599 12.8549 15.8537C12.9443 15.9475 13.0656 16.0001 13.1921 16.0001C13.3186 16.0001 13.4398 15.9475 13.5293 15.8537C13.6187 15.7599 13.6689 15.6327 13.6689 15.5001C13.6666 14.1401 13.2915 12.8095 12.5881 11.6668C12.5086 11.7835 12.4133 11.8918 12.3338 12.0085C12.1191 11.7564 11.8668 11.5425 11.5868 11.3751Z" fill="#464646"/>
                        <path d="M6.83449 8.33325C6.08836 8.33521 5.34752 8.46469 4.64111 8.71659C5.30798 9.12032 6.06445 9.33287 6.83449 9.33287C7.60453 9.33287 8.361 9.12032 9.02787 8.71659C8.32146 8.46469 7.58062 8.33521 6.83449 8.33325Z" fill="#464646"/>
                        <path d="M11.5869 11.375C11.8658 11.5373 12.118 11.7455 12.3339 11.9917C12.4134 11.875 12.5088 11.7667 12.5882 11.65C12.4142 11.36 12.2231 11.0817 12.0161 10.8167C11.873 11.0083 11.7141 11.1833 11.5869 11.375Z" fill="#464646"/>
                        </svg>
                        <svg xmlns="http://www.w3.org/2000/svg" width="14" height="16" viewBox="0 0 14 16" fill="none">
                        <path d="M3.33792 4.66668C3.33792 3.94148 3.543 3.23257 3.92722 2.62959C4.31144 2.02661 4.85755 1.55665 5.49649 1.27912C6.13542 1.0016 6.83849 0.928991 7.51678 1.07047C8.19507 1.21195 8.81812 1.56117 9.30714 2.07396C9.79616 2.58675 10.1292 3.24009 10.2641 3.95135C10.399 4.66262 10.3298 5.39986 10.0651 6.06986C9.80047 6.73985 9.35229 7.31251 8.77727 7.7154C8.20224 8.1183 7.52619 8.33335 6.83461 8.33335C7.58074 8.33531 8.32158 8.46479 9.02799 8.71668C9.88314 8.20875 10.5539 7.41828 10.9356 6.4686C11.3173 5.51892 11.3885 4.46346 11.138 3.4669C10.8875 2.47035 10.3295 1.58876 9.55106 0.959705C8.77258 0.330647 7.81742 -0.010498 6.83461 -0.010498C5.85181 -0.010498 4.89664 0.330647 4.11816 0.959705C3.33968 1.58876 2.78168 2.47035 2.53122 3.4669C2.28076 4.46346 2.35193 5.51892 2.73363 6.4686C3.11533 7.41828 3.78608 8.20875 4.64123 8.71668C5.34764 8.46479 6.08848 8.33531 6.83461 8.33335C5.90723 8.33335 5.01783 7.94704 4.36208 7.25941C3.70632 6.57177 3.33792 5.63914 3.33792 4.66668Z" fill="#464646"/>
                        <path d="M0 15.5001C0 15.6327 0.0502364 15.7599 0.139658 15.8537C0.229079 15.9475 0.35036 16.0001 0.476821 16.0001C0.603282 16.0001 0.724563 15.9475 0.813985 15.8537C0.903406 15.7599 0.953642 15.6327 0.953642 15.5001C0.955745 13.8653 1.576 12.2981 2.67841 11.1421C3.78082 9.98608 5.2754 9.33567 6.83444 9.33346C6.06412 9.33533 5.30717 9.12251 4.64106 8.7168C3.29059 9.20059 2.11768 10.1141 1.28577 11.33C0.453864 12.5459 0.0043954 14.0037 0 15.5001H0Z" fill="#464646"/>
                        <path d="M11.5868 11.3751C11.7139 11.1835 11.8729 11.0085 12.0159 10.8335C11.2157 9.86347 10.1847 9.13313 9.02785 8.7168C8.36174 9.12251 7.60479 9.33533 6.83447 9.33346C8.39351 9.33567 9.88809 9.98608 10.9905 11.1421C12.0929 12.2981 12.7132 13.8653 12.7153 15.5001C12.7153 15.6327 12.7655 15.7599 12.8549 15.8537C12.9443 15.9475 13.0656 16.0001 13.1921 16.0001C13.3186 16.0001 13.4398 15.9475 13.5293 15.8537C13.6187 15.7599 13.6689 15.6327 13.6689 15.5001C13.6666 14.1401 13.2915 12.8095 12.5881 11.6668C12.5086 11.7835 12.4133 11.8918 12.3338 12.0085C12.1191 11.7564 11.8668 11.5425 11.5868 11.3751Z" fill="#464646"/>
                        <path d="M6.83449 8.33325C6.08836 8.33521 5.34752 8.46469 4.64111 8.71659C5.30798 9.12032 6.06445 9.33287 6.83449 9.33287C7.60453 9.33287 8.361 9.12032 9.02787 8.71659C8.32146 8.46469 7.58062 8.33521 6.83449 8.33325Z" fill="#464646"/>
                        <path d="M11.5869 11.375C11.8658 11.5373 12.118 11.7455 12.3339 11.9917C12.4134 11.875 12.5088 11.7667 12.5882 11.65C12.4142 11.36 12.2231 11.0817 12.0161 10.8167C11.873 11.0083 11.7141 11.1833 11.5869 11.375Z" fill="#464646"/>
                        </svg>
                        <div class="contenedor_principal--sub">
                            {{JSON.parse(actividad.activity).subtitle}}
                        </div>
                </div>
                 <div class="contenedor_principal--direccion">
                    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="24" viewBox="0 0 16 24" fill="none">
                        <path fill-rule="evenodd" clip-rule="evenodd" d="M8.22125 9.6929C7.26176 9.6929 6.44781 8.9098 6.44781 7.92403C6.44781 6.96743 7.23249 6.15594 8.22125 6.15594C9.18154 6.15594 9.99548 6.93826 9.99548 7.92403C9.99548 8.9098 9.18154 9.6929 8.22125 9.6929ZM8.22162 4.84937C6.53508 4.84937 5.13965 6.24127 5.13965 7.92259C5.13965 9.60471 6.53508 10.9966 8.22162 10.9966C9.90895 10.9966 11.3044 9.60471 11.3044 7.92259C11.3044 6.24127 9.90895 4.84937 8.22162 4.84937Z" fill="#464646"/>
                        <path fill-rule="evenodd" clip-rule="evenodd" d="M8.22076 21.8121L2.54981 10.8526C2.08467 9.9536 1.85132 8.96783 1.85132 7.92448C1.85132 4.41591 4.73149 1.54611 8.25003 1.54611C11.7686 1.54611 14.6479 4.41591 14.6479 7.92448C14.6479 8.93944 14.4154 9.92521 13.9503 10.8235L8.22076 21.8121ZM15.9291 7.92305C15.9291 3.68972 12.4683 0.239502 8.22195 0.239502C3.97643 0.239502 0.515625 3.68972 0.515625 7.92305C0.515625 9.14068 0.805937 10.3875 1.38735 11.46L7.64054 23.5504C7.75682 23.7822 7.98939 23.8982 8.22195 23.8982C8.45452 23.8982 8.68788 23.7531 8.80337 23.5504L11.9446 17.5052L15.0858 11.46C15.638 10.3583 15.9291 9.14068 15.9291 7.92305Z" fill="#464646"/>
                    </svg>
                    <div class="principal--direccion--caba">
                        {{JSON.parse(actividad.activity).address}} {{JSON.parse(actividad.activity).locations[0].province}}
                    </div>
                </div>
                </div>
                 <div class="contenedor_principal--puntos">{{actividad.points}} puntos</div>

        <h1 class="titulo">¿Qué incluye?</h1>   

        <div class="barra">
            <svg xmlns="http://www.w3.org/2000/svg" width="157" height="4" viewBox="0 0 157 4" fill="none">
            <rect x="0.0742188" y="0.469482" width="156.116" height="2.9931" fill="#FF6C5F"/>
            </svg>
        </div>
        
        <div class="contenedor_incluye">
           <ul class="contenedor_incluye--info">
                <li v-html="JSON.parse(actividad.activity).benefits.substr(JSON.parse(actividad.activity).benefits.indexOf(''), JSON.parse(actividad.activity).benefits.indexOf('.')+1)"></li>
                <li v-html="JSON.parse(actividad.activity).benefits.substr(JSON.parse(actividad.activity).benefits.lastIndexOf('. ')+1,JSON.parse(actividad.activity).benefits.indexOf('.'))"></li>
            </ul>
        </div>

        <div class="contenedor_beneficios" v-html="JSON.parse(actividad.activity).benefits.substr(JSON.parse(actividad.activity).benefits.indexOf('H'),JSON.parse(actividad.activity).benefits.indexOf('.'))"></div>
       
        <div class="contenedor_reglas">
            <div class="reglas">
                <div>
                    <svg xmlns="http://www.w3.org/2000/svg" width="20" height="26" viewBox="0 0 20 26" fill="none">
                    <g id="Reglas">
                    <path id="Shape" d="M4.06654 9.66678H8.99987C9.26654 9.66678 9.5332 9.40011 9.5332 9.13345C9.5332 8.86678 9.26654 8.73345 8.99987 8.73345H4.06654C3.79987 8.73345 3.5332 9.00011 3.5332 9.26678C3.5332 9.53345 3.79987 9.66678 4.06654 9.66678Z" fill="#464646"/>
                    <path id="Shape_1_" d="M19 8.73333C18.7333 8.73333 18.4667 9 18.4667 9.26667V24.0667H2.06667V2.06667H13.4C13.6667 2.06667 13.9333 2.2 14.0667 2.33333L17.8 6.2H14.4667V4.06667C14.4667 3.8 14.2 3.53333 13.9333 3.53333C13.6667 3.53333 13.4 3.8 13.4 4.06667V6.46667C13.4 6.86667 13.8 7.26667 14.2 7.26667H18.3333C18.6 7.26667 18.8667 7.13333 19 6.73333C19.1333 6.46667 19 6.06667 18.8667 5.93333L14.7333 1.66667C14.3333 1.26667 13.8 1 13.2667 1H1.8C1.4 1 1 1.4 1 1.8V24.2C1 24.6 1.4 25 1.8 25H18.6C19 25 19.4 24.6 19.4 24.2V9.13333C19.5333 8.86667 19.2667 8.73333 19 8.73333Z" fill="#464646" stroke="#464646" stroke-width="0.3"/>
                    <path id="Shape_2_" d="M4.06654 21.4002C3.79987 21.4002 3.5332 21.6668 3.5332 21.9335C3.5332 22.2002 3.79987 22.4668 4.06654 22.4668H8.99987C9.26654 22.4668 9.5332 22.2002 9.5332 21.9335C9.5332 21.6668 9.26654 21.4002 8.99987 21.4002H4.06654Z" fill="#464646"/>
                    <path id="Shape_3_" d="M16.8665 19.4001C16.8665 19.1334 16.5999 18.8667 16.3332 18.8667H4.06654C3.79987 18.8667 3.5332 19.1334 3.5332 19.4001C3.5332 19.6667 3.79987 19.9334 4.06654 19.9334H16.4665C16.7332 19.8001 16.8665 19.6667 16.8665 19.4001Z" fill="#464646"/>
                    <path id="Shape_4_" d="M16.4665 11.1336H4.06654C3.79987 11.1336 3.5332 11.4002 3.5332 11.6669C3.5332 11.9336 3.79987 12.2002 4.06654 12.2002H16.4665C16.7332 12.2002 16.9999 11.9336 16.9999 11.6669C16.8665 11.4002 16.7332 11.1336 16.4665 11.1336Z" fill="#464646"/>
                    <path id="Shape_5_" d="M16.4665 13.7996H4.06654C3.79987 13.7996 3.5332 14.0663 3.5332 14.3329C3.5332 14.5996 3.79987 14.8663 4.06654 14.8663H16.4665C16.7332 14.8663 16.9999 14.5996 16.9999 14.3329C16.8665 14.0663 16.7332 13.7996 16.4665 13.7996Z" fill="#464646"/>
                    <path id="Shape_6_" d="M16.4665 16.3333H4.06654C3.79987 16.3333 3.5332 16.6 3.5332 16.8666C3.5332 17.1333 3.79987 17.4 4.06654 17.4H16.4665C16.7332 17.4 16.9999 17.1333 16.9999 16.8666C16.8665 16.6 16.7332 16.3333 16.4665 16.3333Z" fill="#464646"/>
                    </g>
                    </svg>
                </div>
                <div class="reglas_titulo">
                    Reglas:
                </div>
            </div>
            <div class="lorem">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aperiam provident fugit necessitatibus inventore temporibus nostrum eligendi. Ex qui repellendus voluptas quisquam laudantium sequi quaerat! Perspiciatis facere voluptas fuga cum nesciunt?</div>    
        </div>

        <h1 class="actividades_titulo">Otras actividades similares:</h1>

        <div class="contenedor_otras"> 
            <OtrasActividades/>
        </div>

    </div>
</template>

<script>

import OtrasActividades from '../otrasActividades/otrasActividades.vue'
 
export default {
    name:'ActividadesDetalle',
    components:{
        OtrasActividades,   
    },
    data(){
        return{
            id: this.$router.currentRoute.params.id,
            actividad:"",
        }
    },
    mounted(){
        fetch(`https://json-biglifeapp.herokuapp.com/activity/${this.id}`)
        .then((response)=> response.json())
        .then ((data)=> (this.actividad=data))
    }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Quicksand&display=swap');
.contenedor_principal{
    position: absolute;
    width: 196px;
    height: 38px;
    left: 696px;
    top: 111px;
}
.contenedor_principal--titulo{
    font-family: Quicksand;
    font-style: normal;
    font-weight: bold;
    font-size: 30px;
    line-height: 37px;
    letter-spacing: -1px;
    color: #464646;
}
.contenedor_principal--descrip{
    font-family: Quicksand;
    font-style: normal;
    font-weight: normal;
    font-size: 18px;
    line-height: 22px;
    color: #4F4F4F;
}
.contenedor_detalle--imagen{
    position: absolute;
    width: 563px;
    height: 371px;
    left: 100px;
    top: 111px;
    border-radius: 4px;
}
.contenedor_principal--direccion{
    display: flex;
    flex-direction: row;
    justify-content: initial;
}
.principal--direccion--caba{
    font-family: Quicksand;
    font-style: normal;
    font-weight: normal;
    font-size: 16px;
    line-height: 20px;
    text-align: center;
    color: #464646;
    margin-left: 12px;
}
.contenedor_principal--puntos{
    position: absolute;
    width: 137px;
    height: 30px;
    left: 698px;
    top: 384px;
    font-family: Quicksand;
    font-style: normal;
    font-weight: normal;
    font-size: 24px;
    line-height: 30px;
    color: #464646;
}
.contenedor_principal--subtitle{
    display: flex;
    flex-direction: row;
}
.contenedor_principal--sub{
    font-family: Quicksand;
    font-style: normal;
    font-weight: normal;
    font-size: 16px;
    line-height: 20px;
    color: #464646;
    margin-left:12px;
}
.titulo{
    position: absolute;
    height: 57px;
    left: 8.36%;
    right: 80.46%;
    top: 579px;
    font-family: Quicksand;
    font-style: normal;
    font-weight: 500;
    font-size: 22px;
    line-height: 27px;
    letter-spacing: -1px;
    color: #464646;
}
.barra{
    position: absolute;
    left: 7.41%;
    right: 81.04%;
    margin-top: 616px;
    bottom: 63.18%;
}
.contenedor_incluye{
    position: absolute;
    width: 565px;
    height: 100px;
    left: 100px;
    top: 671px;
    display: grid;
}
.contenedor_incluye--info{
    margin-left: 40px;
    font-family: Quicksand;
    font-style: normal;
    font-weight: 300;
    font-size: 18px;
    line-height: 22px;
    color: #4F4F4F;
}
.contenedor_beneficios{
    position: absolute;
    width:564px;
    height:82px;
    top:790px;
    margin-left: 110px;
    font-family: Quicksand;
    font-style: normal;
    font-weight: 300;
    font-size: 18px;
    line-height: 22px;
    color: #4F4F4F;
}
.contenedor_reglas{
    position: absolute;
    margin-top:920px;
    margin-left: 100px; 
}
.reglas{
    display: flex;
    flex-direction: row;
    align-items: center;
    align-content: space-between;
    align-items: space-between;
}
.reglas_titulo{
    font-family: Quicksand;
    font-style: normal;
    font-weight: bold;
    font-size: 22px;
    line-height: 27px;
    letter-spacing: -1px;
    color: #464646;
    margin-left:19px;
}
.lorem{
    margin-top:15px;
    font-family: Quicksand;
    font-style: normal;
    font-weight: 300;
    font-size: 18px;
    line-height: 22px;
    color: #4F4F4F;
}
.actividades_titulo{
    position: absolute;
    margin-top:1111px;
    margin-left: 100px;
    font-family: Quicksand;
    font-style: normal;
    font-weight: bold;
    font-size: 24px;
    line-height: 30px;
    letter-spacing: -1px;
    color: #464646;
}
.contenedor_otras{
    position:absolute;
    margin-top: 1158px;
    margin-left: 100px;
}
.barra{
    position:absolute;
    top: 1px;
    margin-left: 15px;
}
.control{
    height: 200px;
    position: absolute;
    margin-top: 111px;
    margin-left:696px;
    display: grid;
    grid-template-columns: auto;
    align-content: space-between;
}
</style>
