# Siarhei Siarheyeu #
### Junior Frontend Developer ###
## Contact information: ##
* **Email:** awer100@gmail.com </br>
* **Phone:** +1 (720) 869-1895 </br>
* **Discord:** zyvie-by#3664 </br>
[Linkedin](https://www.linkedin.com/in/siarhei-siarheyeu-339463170/)
## Skills and Proficiency: ##
* HTML5, CSS3, SCSS </br>
* Bootstrap, Swiper </br>
* VS Code, Git, GitHub </br>
* Figma, Photoshop, CorelDRAW </br>
## About me: ##
<p>Over 14 years experience in design. Development of flyers, business cards, banners, stickers for transport. Extensive experience in Photoshop, CorelDRAW, Figma.</p>

## Interest: ##
<p>photography, chess, auto-travel.</p>

## Courses ##
* "Website development using HTML, CSS and JavaScript". it-academy Minsk. November 2021- March 2022 [Diploma]().</br>**COMPLETED**
* "Developing Web Applications with JavaScript". it-academy Minsk. November 2021- March 2022. </br>
*In connection with the move, I did not have time to defend my diploma.* </br>**COMPLETED**
* English language course based on Cherokee Trail High School. From January 2023. </br> *IN PROGRESS*
* RS Schools JavaScript/Front-end. From March 2023. </br> *IN PROGRESS*

## Code example: ##
[This is the code snippet I used in my project. Accepts parameters FORM and JSON. Outputs Swiperjs](https://awer17.github.io/Nails_club/)

```
function initSliders() {
    if (document.querySelector('.mySwiper')) { 
        async function getSliderProducts() {
            
            const file = 'json/listmaster.json';
            let response = await fetch(file, {
                method: 'GET'
            });
            if(response.ok) {
                let result = await response.json();
                loadSliderProducts(result);
                
                ;
            } else {
                throw new Error(`!!!!!!!!!!! ${err}`)
            }
        }
    
        function loadSliderProducts(data) {
            
            const sliderBody = document.querySelector('.master_list');
            sliderBody.innerHTML = '';

            data.forEach(item => {
                const servis = Object.keys(item.servis[0])[0]
                const servisItem =Object.values(item.servis[0])[0]
                const imgFoto = item.imges;
                const idMaster = item.id
                const imgesFoto =  document.createElement('div')
                const nameMaster = item.firstName


                if((serviselist.value == servis || serviselist.value == "start" ) && (servisItem.includes(itemChoice) || servisItemlist.value == "start") && (nameList.value == "start" || nameList.value == nameMaster) )  {
                    imgFoto.forEach(item =>{
                    imgesFoto.textContent += `<div class="swiper-slide"><img src="imeges/masters/${idMaster}/${item}" alt="nails"></div>`})
                    sliderBody.innerHTML += `
                    <div class="swiper-slide item_master">
                    <div class="slaider_item">
                        <img src="imeges/masters/${idMaster}/${item.img}" alt="foto_master">
                        <div class="items_content">
                            <div>
                                <h2 class="first_name">
                                    ${item.firstName} ${item.lastName}
                                </h2>
                                <p class="typye_work">
                                    ${item.speciality}
                                </p>
                            </div>
                            <ul class="service_info">
                                <li>${item.skill[0]}</li>
                                <li>${item.skill[1]}</li>
                                <li>${item.skill[2]}</li>
                            </ul>
                        </div>
                        <div class="title">${item.aboutMe} </div>
                        <div class="swiper mySwiper2 wrap_swiper2 ">
                                        <div class="swiper-wrapper imges_item ">
                                            ${imgesFoto.textContent}                            
                                    </div>
                            <div class="swiper-pagination " id="elem"></div>
                            </div>
                        </div>
                        <div class="imges_item">   
                    </div>
                </div>` 
                }  
                
                var swiper1 = new Swiper(".mySwiper2", {
                    slidesPerView: 4,
                    spaceBetween: 13,
                    pagination: {
                        el: ".swiper-pagination",
                        type: "progressbar",
                    },
                    grabCursor: true,
                    observeSlideChildren: true,
                    observer: true,
                    observeParents:true,
                });    
                
                if( (nameList.value === 'start' && servisItemlist.value === "start") || (serviselist.value == servis && servisItem.includes(itemChoice) )|| (serviselist.value == servis && servisItemlist.value === "start") ){
                    var itemsFirsName = document.querySelectorAll(".first_name")
                    nameList.innerHTML = `<option value="start" >select from the list</option>`
                    itemsFirsName.forEach(item => {
                        nameList.innerHTML += `<option value=${item.innerHTML}>${item.innerHTML}</option>`
                    })
                    nameList.firstElementChild.setAttribute("disabled", "disabled")
                }
            })
        }
        getSliderProducts();
}}
```


