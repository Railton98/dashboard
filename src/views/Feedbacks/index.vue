<template>
  <div class="flex justify-center w-full h-28 bg-brand-main">
    <header-logged />
  </div>

  <div class="flex flex-col items-center justify-center h-64 bg-brand-gray">
    <h1 class="text-4xl font-black text-center text-gray-800">
      Feedbacks
    </h1>
    <p class="text-lg text-center text-gray-800 font-regular">
      Detalhes de todos os feedbacks recebidos.
    </p>
  </div>

  <div class="flex justify-center w-full pb-20">
    <div class="grid w-4/5 max-w-6xl grid-cols-4 gap-2 py-10">
      <div>
        <h1 class="text-3xl font-black text-brand-darkgray">
          Listagem
        </h1>
        <suspense>
          <template #default>
            <filters />
          </template>
          <template #fallback>
            carregando...
          </template>
        </suspense>
      </div>
      <div class="col-span-3 px-10 pt-20"></div>
    </div>
  </div>
</template>

<script>
import HeaderLogged from '../../components/HeaderLogged'
import Filters from './Filters'

export default {
  components: { HeaderLogged, Filters }
}
</script>
