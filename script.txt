let current=0;
const screens=document.querySelectorAll(".screen");

function nextScreen(){
screens[current].classList.remove("active");
current++;
if(current>=screens.length) current=screens.length-1;
screens[current].classList.add("active");
}

const images=["a.jpg","b.jpg","c.jpg","d.jpg"];
let slideIndex=0;
setInterval(()=>{
if(screens[1].classList.contains("active")){
slideIndex=(slideIndex+1)%images.length;
document.getElementById("slide").src=images[slideIndex];
}
},2000);

function celebrate(){
document.getElementById("finalMsg").innerText="Forever Yours Samira Jaan ♾️❤️";
}

setInterval(()=>{
let p=document.createElement("div");
p.className="petal";
p.innerText="🌹";
p.style.left=Math.random()*100+"%";
document.body.appendChild(p);
setTimeout(()=>p.remove(),6000);
},800);
