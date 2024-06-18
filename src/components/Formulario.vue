<script setup>
    const props = defineProps (['CadastraTarefa', 'TarefaTemp', 'TrocarFiltro', 'editaTarefaTemp' ])
</script>

<template>
    <form @submit.prevent="props.CadastraTarefa">
        <div class="row">
            <div class="col">
                <input :value="props.TarefaTemp" @change="props.editaTarefaTemp"
                    required type="text" placeholder="Digite a descrição da tarefa" class="form-control" />
            </div>
            <div class="col md-2">
                <button type="submit" class="btn btn-primary">Cadastrar</button>
            </div>
            <div class="col mb-2">
                <select @change="props.TrocarFiltro" class="form-control">
                    <option value="todas">Todas tarefas</option>
                    <option value="pendentes">Pendentes</option>
                    <option value="finalizadas">Finalizadas</option>
                </select>
            </div>
        </div>
    </form>
</template>
