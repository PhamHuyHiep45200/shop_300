<template>
  <div className="flex justify-center">
      <div className="mb-[100px] mt-[50px] w-[1280px] relative px-2 sm:px-0">
        <div className="flex items-center justify-center mb-5">
          <div className="flex items-center">
            <span className="text-[40px] font-semibold">Giỏ Hàng</span>
            <img src="/image/cart.gif" />
          </div>
        </div>
        <a-button danger className="my-2 float-right">
          Xoá Sản Phẩm
        </a-button>
        <!-- <Table
          rowSelection={rowSelection}
          columns={columns}
          dataSource={carts}
          pagination={false}
          scroll={{ x: 400 }}
        /> -->
        <div className="sticky bottom-0 h-[140px] bg-white border-t-[2px] flex flex-col items-end justify-center">
          <span>
            Tổng Tiền:{" "}
            <span className="text-primary text-[20px] font-bold">
              {{formatMoney(totalPrice)}}đ
            </span>
          </span>
          <a-button
            className="bg-primary text-white !px-[30px] mt-[10px] hover:!text-white"
            size="large"
          >
            Mua Hàng
          </a-button>
        </div>
      </div>
    </div>
</template>

<script lang="ts" setup>
import { formatMoney } from '~/common/common';

defineProps<{
  detail: any;
}>();
</script>
