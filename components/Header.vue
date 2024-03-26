<template>
  <div
    class="fixed top-0 left-0 right-0 z-[1000] bg-[white] flex justify-center px-5 xl:px-0"
    :style="{
      boxShadow: '0 0 10px 5px #999',
    }"
  >
    <div class="w-[1280px] flex justify-between items-center">
      <div class="hidden md:block">
        <a-image
          class="cursor-poniter max-w-[160px] max-h-[200px]"
          src="/images/logo.jpg"
          alt="logo"
          :preview="false"
        />
      </div>
      <div class="flex justify-center items-center space-x-2">
        <a-input size="large" class="w-[400px]" />
        <a-button class="flex items-center justify-center" size="large"><SearchOutlined/></a-button>
      </div>
      <div class="flex items-center space-x-3 md:space-x-6">
        <a-badge :count="2">
          <BellOutlined class="text-[22px]" />
        </a-badge>
        <a-badge :count="10">
          <ShoppingCartOutlined class="text-[25px]" />
        </a-badge>
        <!-- <div class="items-center cursor-pointer hidden md:flex">
              <Tooltip
                class="space-x-1"
                title={
                  <div>
                    <div
                      class="text-[#333] px-5 py-2 cursor-pointer"
                      onClick={() => {
                        redirectRouter("/info-me");
                      }}
                    >
                      Thông Tin Của Tôi
                    </div>
                    <div
                      class="text-[#333] px-5 py-2 cursor-pointer"
                      onClick={() => {
                        redirectRouter("/order-me");
                      }}
                    >
                      Đơn Hàng Của Tôi
                    </div>
                    <div
                      class="text-[#333] px-5 py-2 cursor-pointer"
                      onClick={() => {
                        redirectRouter("/order-me");
                      }}
                    >
                      Đơn Hàng Đã Đăng Bán
                    </div>
                    <div
                      class="text-[#333] px-5 py-2 cursor-pointer"
                      onClick={() => {
                        redirectRouter("/login");
                        resetStore();
                      }}
                    >
                      Đăng Xuất
                    </div>
                  </div>
                }
                color="white"
              >
                <Avatar src={user?.image}>{user?.name?.[0]}</Avatar>
                <span>{user.name}</span>
              </Tooltip>
            </div> -->
      </div>
    </div>
    <Drawer placement="left" width="80%" v-if="false">
      <div class="flex justify-center mb-5">
        <a-image
          class="cursor-poniter"
          :width="160"
          :height="200"
          src="/images/logo.jpg"
          alt="logo"
        />
      </div>
      <div>
        <div class="text-[#333] px-5 py-2 cursor-pointer font-semibold">
          Thông Tin Của Tôi
        </div>
        <Divider class="!my-0" />
        <div class="text-[#333] px-5 py-2 cursor-pointer font-semibold">
          Đăng Bán Sản Phẩm
        </div>
        <Divider class="!my-0" />
        <div class="text-[#333] px-5 py-2 cursor-pointer font-semibold">
          Đơn Hàng Của Tôi
        </div>
        <Divider class="!my-0" />
        <div class="text-[#333] px-5 py-2 cursor-pointer font-semibold">
          Đơn Hàng Đã Đăng Bán
        </div>
        <Divider class="!my-0" />
        <div class="text-[#333] px-5 py-2 cursor-pointer font-semibold">
          Đăng Xuất
        </div>
      </div>
    </Drawer>
  </div>
</template>
