.box {
    width: 150px;
    height: 150px;
    background: #145a32;
    position: relative;
    cursor: pointer;
    border-radius: 10px;
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;
    font-weight: bold;
}

.lid {
    position: absolute;
    width: 150px;
    height: 40px;
    background: #1e8449;
    top: -40px;
    border-radius: 10px 10px 0 0;
    transition: 0.5s;
}

.open .lid {
    transform: rotateX(120deg);
    transform-origin: bottom;
}

.baby {
    display: none;
    text-align: center;
}

.baby img {
    width: 120px;
}

.baby p {
    color: white;
    font-size: 18px;
    margin-top: 10px;
    font-weight: bold;
}

.confetti {
    position: absolute;
    width: 10px;
    height: 10px;
    background: yellow;
    animation: fall 3s linear infinite;
}

@keyframes fall {
    from { transform: translateY(-100px); }
    to { transform: translateY(100vh); }
}
