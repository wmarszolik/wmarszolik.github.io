*{
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}
body {
    font-family: "Poppins", sans-serif;
    --color1: #FFF ;
    --color2: #8399B3 ;
    background-color: #D6E4E5 ;
}
nav {
    max-width: 1368px;
    margin:3px 0px 0px 0px;
    padding: 0px 10px 0px 10px;

}
.nav-bar {
    border-radius: 20px;
    padding: 10px 30px;
    box-shadow: rgba(50, 50, 93, 0.25) 0px 13px 27px -5px, rgba(0, 0, 0, 0.3) 0px 8px 16px -8px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    list-style: none;
    position: relative;
    background-color: var(--color2);
}
.logo img {height: 90px;}
.menu {display: flex;}
.menu li {padding-left: 30px;}
.fa-home {
  background-color: #0b0d17;
  color: #fff;
  font-size: 22px;
  padding: 19px;
}
.menu li a {
    display: inline-block;
    text-decoration: none;
    color: var(--color1);
    text-align: center;
    transition: 0.15s ease-in-out;
    position: relative;
    text-transform: uppercase;
}
.menu li a::after {
    content: "";
    position: absolute;
    bottom: 0;
    left: 0;
    width: 0;
    height: 1px;
    background-color: var(--color1);
    transition: 0.15s ease-in-out;
}
.menu li a:hover:after {width: 100%;}
.open-menu , .close-menu {
    position: absolute;
    color: var(--color1);
    cursor: pointer;
    font-size: 1.5rem;
    display: none;
}
.open-menu {
    top: 50%;
    right: 20px;
    transform: translateY(-50%);
}
.close-menu {
    top: 30px;
    right: 20px;
}
#check {display: none;}

.content {
    max-width: 1368px;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    background-color: #D6E4E5;
}
.card {
    display: flex;
    width: 100vw;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    box-shadow: rgba(50, 50, 93, 0.25) 0px 13px 27px -5px, rgba(0, 0, 0, 0.3) 0px 8px 16px -8px;
    background-color: #FFE3E1;
    border-radius: 20px;
    padding: 10px;
    margin: .6rem .6rem .3rem .6rem;
}
.imagewrapper {
    display: flex;
    max-width: 100vw;
    margin-bottom: 5px;
    
}
.imagewrapper img {
    max-width: 100%;
    border-radius: 15px;
    border: 1px solid #d5bcbc;
}
.card ul {
    width: 100%;
    margin-top: 5px;
    background-color: #efefef;
    border-radius: 15px;
    border: 1px solid #d5bcbc;
}
.card ul li {
    font-size: 1.2rem;
    margin-left: 20px;
    padding: 10px 8px 8px 0px;
}
@media(max-width: 767px){
    .logo img {height: 80px;}
    .menu {
        flex-direction: column;
        align-items: center;
        justify-content: center;
        width: 80%;
        height: 100vh;
        position: fixed;
        top: 0;
        right: -100%;
        z-index: 100;
        background-color: var(--color2);
        transition: all 0.2s ease-in-out;
    }
    .menu li {margin-top: 40px;}
    .menu li a {padding: 10px;}
    .open-menu , .close-menu {display: block;}
    #check:checked ~ .menu {right: 0;}
}
@media(min-width: 768px) {
    .card {
        flex-direction: row;
    }
    .card ul {
        height: 100%;
        width: auto;
        margin-left: 5px;
        margin-top: 0px;
        flex-shrink: 2;
    }
    .imagewrapper {
        margin-right: 5px;
        margin-bottom: 0px;
        flex-shrink: 3;
    }
}
