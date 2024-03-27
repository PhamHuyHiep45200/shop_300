<template>
  <div>
    <div className="my-5 font-[500] text-center text-[30px]">Đăng Nhập</div>
    <a-input size="large" placeholder="Email" className="round-[15px]" />
    <a-input-password size="large" placeholder="Mật khẩu" />
    <a-button
      className="w-full !bg-primary !my-2 !font-medium !text-[white] !rounded-[20px]"
      size="large"
    >
      Đăng Nhập
    </a-button>
    <span
      className="block text-right text-primary underline underline-offset-1 cursor-pointer font-medium"
      @click="redirectRegister"
    >
      Đăng kí tài khoản
    </span>
  </div>
</template>

<script lang="ts" setup>
definePageMeta({
  layout: "login",
});

const router = useRouter();

const redirectRegister = () => {
  router.push("/register");
};
</script>
