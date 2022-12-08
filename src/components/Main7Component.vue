<template>
    <div class="bggg container-fluid mt-5 pt-5 mb-5 pb-5">
        <div class="text-center">
            <h1>Subscribe<mark>Newsletters</mark></h1>
        </div>
        <div class="text-center pt-3">
            <h5>Enter your email address to register to our newsletter subscription<br>delivered on a regular basis!
            </h5>
            <form>
                <div class="mb-3 mt-5 d-flex justify-content-around">
                    <input placeholder="Enter your email" type="email" class="form-control" id="exampleInputEmail1"
                        aria-describedby="emailHelp">
                    <span class="button">
                        <a class="text-white" href="#nogo">Subscribe</a>
                    </span>
                </div>
            </form>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@use '../assets/partials/mixins' as *;
@use '../assets/partials/variables' as *;

.bggg {
    background-color: $col1;
}

h1 {
    font-weight: bold;
    color: $col1-2;
}

mark {
    background-color: $col1;
    font-weight: 400;
    color: $col4;
}

input {
    height: 50px;
    width: 430px;
}

.button {
    margin-left: -920px;
    font-weight: bold;
    padding: 12px;
    background-color: $col4;
    border-radius: 4%;
    width: 10%;
    transition: .2s;

    &:hover {
        background-color: $col1-1;
    }

    a {
        text-decoration: none;
    }
}
</style>