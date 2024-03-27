<template>
    <div>
      <div className="my-5 font-[500] text-center text-[30px]">Đăng Ký Khoản</div>
      <a-input size="large" placeholder="Tên" />
      <a-input-password size="large" placeholder="Mật khẩu" />
      <a-input-password size="large" placeholder="Nhập lại mật khẩu" />
        <a-button
          className="w-full !bg-primary !text-[white] !my-3"
          size="large"
          htmlType="submit"
        >
          Đăng kí
        </a-button>
        <span
          className="block text-right underline cursor-pointer underline-offset-1 text-primary font-medium"
          @click="redirectLogin"
        >
          Đăng nhập
        </span>
    </div>
</template>

<script lang="ts" setup>
definePageMeta({
  layout: "login",
});

const router = useRouter();

const redirectLogin = () => {
  router.push("/login");
};
</script>
