<template>
    <div class="privacy-wrap">
        <h3>개인정보 입력 후 시승신청 버튼을 눌러주세요.</h3>
        <form>
            <fieldset>
                <legend>시승신청</legend>
                <!-- <dl>
                    <dt>시승희망일</dt>
                    <dd>
                        <select name="month" id="month">
                            <option value="" disabled selected>월 선택</option>
                            <option value="2">2</option>
                            <option value="3">3</option>
                        </select>
                        <select name="day" id="day">
                            <option value="" disabled selected>일 선택</option>
                            <option value="1">1</option>
                            <option value="2">2</option>
                            <option value="3">3</option>
                        </select>
                    </dd>
                </dl> -->
                <dl>
                    <dt>
                        <labal>이름</labal>
                    </dt>
                    <dd>
                        <input value="이름을 입력해주세요.">
                    </dd>
                </dl>
                <dl>
                    <dt>
                        <labal>연락처</labal>
                    </dt>
                    <dd>
                        <input value="연락처를 입력해주세요.">
                    </dd>
                </dl>
                <dl>
                    <dt>
                        <labal>성별</labal>
                    </dt>
                    <dd>
                        <select>
                            <option value="여자">여자</option>
                            <option value="남자">남자</option>
                        </select>
                    </dd>
                </dl>
                <dl>
                    <dt>
                        <labal>연령</labal>
                    </dt>
                    <dd>
                        <select>
                            <option value="20대">20대</option>
                            <option value="30대">30대</option>
                            <option value="40대">40대</option>
                        </select>
                    </dd>
                </dl>
                <dl>
                    <dt>
                        <labal>메일</labal>
                    </dt>
                    <dd>
                        <input value="mail@example.com">
                    </dd>
                </dl>
                <button>
                    시승신청
                </button>
            </fieldset>
        </form>

    </div>

</template>
<script>
export default {

}
</script>
<style scoped>
.privacy-wrap{
    display: none;
}
h3{
    text-align: center;
    padding:2rem;
}
fieldset{
    width:50vw;
    margin:0 auto;
    border-style: none;
}
legend{
    display: none;
}
input{
    outline-style: solid;
    padding:0.5rem;
}
select{
    outline-style: solid;
    padding:0.5rem;
}
dl{
    display: flex;
    align-items: center;
    margin-bottom:2rem;
}
dt{
    margin-right:1rem;
}
button{
    border-style: solid;
    padding:1rem;
}




</style>
