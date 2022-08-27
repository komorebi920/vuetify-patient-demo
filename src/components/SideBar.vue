<template>
    <v-navigation-drawer app permanent color="#2784FF" mini-variant mini-variant-width="80">
        <v-avatar class="d-block text-center mx-auto mt-4 mb-16" color="" size="40">
            <v-icon color="white" x-large>fab fa-artstation</v-icon>
        </v-avatar>

        <v-list flat class="mt-16">
            <v-list-item-group v-model="selectedItem">
                <v-list-item v-for="(item, i) in items" :key="i" active-class="border" :ripple="false">
                    <v-list-item-icon>
                        <v-icon v-text="item.icon" color="white" />
                    </v-list-item-icon>
                </v-list-item>
            </v-list-item-group>
        </v-list>

        <div style="position: absolute; bottom: 20px; left: 0; right: 0;">
            <v-list-item :ripple="false">
                <v-list-item-icon>
                    <v-icon color="white">fa-solid fa-cog</v-icon>
                </v-list-item-icon>
            </v-list-item>
            <v-list-item :ripple="false">
                <v-list-item-icon>
                    <v-icon color="white">fa-solid fa-info-circle</v-icon>
                </v-list-item-icon>
            </v-list-item>
        </div>
    </v-navigation-drawer>
</template>

<script>
export default {
    data: () => ({
        selectedItem: 3,
        items: [
            { icon: "fa-solid fa-file-medical-alt" },
            { icon: "fa-solid fa-user-nurse" },
            { icon: "fa-solid fa-virus" },
            { icon: "fa-solid fa-user-md" },
            { icon: "fa-solid fa-comment-medical" },
        ],
    }),
};
</script>

<style lang="scss">
.border {
    margin-left: 12px;
    margin-right: 12px;
    background: #529DFF;
    border-radius: 50%;
    text-decoration: none;
}

.v-list-item-group {
    .v-list-item--active {
        color: white !important;
    }

    .v-list-item__icon {
        justify-content: center;
    }
}
</style>