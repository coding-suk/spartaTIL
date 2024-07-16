
# 스파르타 코딩 1주차 늦게 시작한 1일

>계절학기에서 발표 문제로 15일 본 수업이 시작하였지만 나의 시작은 16일 하루 지나고 부터
>시작이다. 

늦게 시작한 탓에 사전수강을 다 못들어서 이번 1주차는 사전 수강을 다 듣는 시간을 갖는다.

 수강 자료는 SQL 과 웹(프론트) 둘 중 수업에 빠르게 참여 할수있다는 웹 부터 수강을 시작한다.

그렇다고 SQL이 덜 중요하다는 뜻은 절대 아님 
원래의 목표는 오늘 웹강의 5주차를 다 끝내는 것이었으나 따라하면서 듣다보니 생각보다 오래 걸렸다.
그래서 수업 시간내에 과제를 쳐 내며 완강한건 3주차,,, 
아직 그래도 오늘이 끝나려면 내가 자기 전까지라 생각하니 좀 더 듣고 자고자 한다.

### 오늘들은 html ### 

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>스파르타플릭스</title>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Gugi&display=swap');

        * {
            font-family: "Gugi", sans-serif;
            font-weight: 400;
            font-style: normal;
        }

        .main {
            background-color: green;
            color: white;

            background-image: url('https://occ-0-1123-1217.1.nflxso.net/dnm/api/v6/6AYY37jfdO6hpXcMjf9Yu5cnmO0/AAAABeIfo7VL_VDyKnljV66IkR-4XLb6xpZqhpLSo3JUtbivnEW4s60PD27muH1mdaANM_8rGpgbm6L2oDgA_iELHZLZ2IQjG5lvp5d2.jpg?r=e6e.jpg');
            background-position: center;
            background-size: cover;

        }

        body {
            background-color: black;
        }

        .mycards {
            width: 1200px;
            margin: 20px auto 20px auto;
        }

        .postingbox {
            width: 500px;

            margin: 20px auto 20px auto;

            border: 1px solid white;
            padding: 20px;
            border-radius: 5px;
            text-align: right;
        }

        .form-floating>input {
            background-color: transparent;
            color: white;
        }

        .form-floating>label {
            color: white;
        }

        .input-group>label {
            background-color: transparent;
            color: white;
        }
    </style>
    <script>
        $(document).ready(function () {
            let url = "http://spartacodingclub.shop/sparta_api/weather/seoul";
            fetch(url).then(res => res.json()).then(data => {
                let temp = data['temp'];
                $('#temperature').text(temp);
            })
        })
        function openclose() {
            $('#postingbox').toggle();
        }
        function makeCard() {
            let image = $('#image').val();
            let title = $('#title').val();
            let star = $('#star').val();
            let comment = $('#comment').val();

            let temp_html =
                `<div class="col">
                <div class="card">
                    <img src="${image}"
                        class="card-img-top" alt="...">
                    <div class="card-body">
                        <h5 class="card-title">${title}</h5>
                        <p class="card-text">${star}</p>
                        <p class="card-text">${comment}</p>
                    </div>
                </div>
            </div>`;
            $('#card').append(temp_html);
        }

    </script>
</head>

<body>
    <header class="p-3 text-bg-dark">
        <div class="container">
            <div class="d-flex flex-wrap align-items-center justify-content-center justify-content-lg-start">
                <a href="/" class="d-flex align-items-center mb-2 mb-lg-0 text-white text-decoration-none">
                    <svg class="bi me-2" width="40" height="32" role="img" aria-label="Bootstrap">
                        <use xlink:href="#bootstrap"></use>
                    </svg>
                </a>

                <ul class="nav col-12 col-lg-auto me-lg-auto mb-2 justify-content-center mb-md-0">
                    <li><a href="#" class="nav-link px-2 text-danger">spartafilx</a></li>
                    <li><a href="#" class="nav-link px-2 text-white">홈</a></li>
                    <li><a href="#" class="nav-link px-2 text-white">시리즈</a></li>
                    <li><a href="#" class="nav-link px-2 text-white">영화</a></li>
                    <li><a href="#" class="nav-link px-2 text-white">내가 찜한 콘텐츠</a></li>
                    <li><a href="#" class="nav-link px-2 text-white">오늘 기온 : <span id="temperature">20.00</span>도</a></li>
                </ul>

                <form class="col-12 col-lg-auto mb-3 mb-lg-0 me-lg-3" role="search">
                    <input type="search" class="form-control form-control-dark text-bg-dark" placeholder="Search..."
                        aria-label="Search">
                </form>

                <div class="text-end">
                    <button type="button" class="btn btn-outline-light me-2">Login</button>
                    <button type="button" class="btn btn-danger">Sign-up</button>
                </div>
            </div>
        </div>
    </header>
    <div class="main">
        <div class="p-5 mb-4 bg-body-tertiary rounded-3">
            <div class="container-fluid py-5">
                <h1 class="display-5 fw-bold">킹덤</h1>
                <p class="col-md-8 fs-4">병든 왕을 둘러싸고 흉흉한 소문이 떠돈다. 어둠에 뒤덮인 조선, 기이한 역병에 신음하는 산하. 정체 모를 악에 맞서 백성을 구원할 희망은 오직
                    세자뿐이다.</p>
                <button onclick="openclose()" type="button" class="btn btn-outline-light">영화 기록하기</button>
                <button type="button" class="btn btn-outline-light">상세정보</button>
            </div>
        </div>
    </div>
    <div class="postingbox" id="postingbox">
        <div class="form-floating mb-3">
            <input type="email" class="form-control" id="image" placeholder="영화 이미지 주소">
            <label for="floatingInput">영화 이미지 주소</label>
        </div>
        <div class="form-floating mb-3">
            <input type="email" class="form-control" id="title" placeholder="영화 제목">
            <label for="floatingInput">영화 제목</label>
        </div>
        <div class="input-group mb-3">
            <label class="input-group-text" for="inputGroupSelect01">별점</label>
            <select class="form-select" id="star">
                <option selected>별점 선택</option>
                <option value="⭐">⭐</option>
                <option value="⭐⭐">⭐⭐</option>
                <option value="⭐⭐⭐">⭐⭐⭐</option>
                <option value="⭐⭐⭐⭐">⭐⭐⭐⭐</option>
                <option value="⭐⭐⭐⭐⭐">⭐⭐⭐⭐⭐</option>
            </select>
        </div>
        <div class="form-floating mb-3">
            <input type="email" class="form-control" id="comment" placeholder="추천 이유">
            <label for="floatingInput">추천 이유</label>
        </div>
        <button onclick="makeCard()" type="button" class="btn btn-danger btn-record">기록하기</button>
    </div>
    <div class="mycards">
        <div id="card" class="row row-cols-1 row-cols-md-4 g-4">
            <div class="col">
                <div class="card">
                    <img src="https://movie-phinf.pstatic.net/20210728_221/1627440327667GyoYj_JPEG/movie_image.jpg"
                        class="card-img-top" alt="...">
                    <div class="card-body">
                        <h5 class="card-title">영화 제목</h5>
                        <p class="card-text">⭐⭐⭐</p>
                        <p class="card-text">영화 코멘트</p>
                    </div>
                </div>
            </div>
            <div class="col">
                <div class="card">
                    <img src="https://movie-phinf.pstatic.net/20210728_221/1627440327667GyoYj_JPEG/movie_image.jpg"
                        class="card-img-top" alt="...">
                    <div class="card-body">
                        <h5 class="card-title">영화 제목</h5>
                        <p class="card-text">⭐⭐⭐</p>
                        <p class="card-text">영화 코멘트</p>
                    </div>
                </div>
            </div>
            <div class="col">
                <div class="card">
                    <img src="https://movie-phinf.pstatic.net/20210728_221/1627440327667GyoYj_JPEG/movie_image.jpg"
                        class="card-img-top" alt="...">
                    <div class="card-body">
                        <h5 class="card-title">영화 제목</h5>
                        <p class="card-text">⭐⭐⭐</p>
                        <p class="card-text">영화 코멘트</p>
                    </div>
                </div>
            </div>
            <div class="col">
                <div class="card">
                    <img src="https://movie-phinf.pstatic.net/20210728_221/1627440327667GyoYj_JPEG/movie_image.jpg"
                        class="card-img-top" alt="...">
                    <div class="card-body">
                        <h5 class="card-title">영화 제목</h5>
                        <p class="card-text">⭐⭐⭐</p>
                        <p class="card-text">영화 코멘트</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</body>

</html>
```
너무 길어서 한개만 올려야 겠다. 생각보다 코딩의 비중보다는 어떤 자료, 사이트에서 끍어 오는게 
많았다. 신기하게도 페이지가 만들어 지드라. 과제 또한 쳐 내봤는데 막상 강의를 듣고나서 좀 쉽네
생각했던 내 자신이 좀 한신하게 느껴질 정도로 못 따라가드라... 

### 진짜 열심히 들었는데... 

무엇보다 이 TIL도 오늘 처음 써본다. 이것도 한번 쓰려고 구글 30분 했따... 
뭔간 좀 한심하게 느껴지긴 한데.. 막상 써보니 괜찮은거 같기도 하고 솔직히 내가 느끼기에 
이래 적는거 아닌거 같아서,, 내일 수업때 피드백좀 제대로 받아보고 싶다. 



