<style scoped>
.spnalign {
    padding-left: 23px;
}
</style>
<template>
    <v-container>
        <v-row>
            <v-col>
                <!-- Niveau 0 -->
                <v-expansion-panels v-model="panelN0">
                    <v-expansion-panel>
                        <v-expansion-panel-title>
                            <v-btn
                                class="text-none text-subtitle-1"
                                size="small"
                                variant="flat"
                                @click.stop="choix(0)"
                            >
                                {{ unitesOrg.nom }}
                            </v-btn>                                                
                        </v-expansion-panel-title>
                        <v-expansion-panel-text>
                            <!-- Niveau 1 directions -->
                            <div v-for="(uo, index) in unitesOrg.enfants" :key="index">
                                <div v-if="uo.enfants.length === 0">
                                    <span class="spnalign"></span>
                                    <v-btn
                                        class="text-none text-subtitle-1"
                                        size="small"
                                        variant="flat"
                                        @click.stop="choix(index)"
                                    >
                                        {{ uo.nom }}
                                    </v-btn>                                                
                                </div>    
                                <div v-else>
                                    <v-expansion-panels>
                                        <v-expansion-panel>
                                            <v-expansion-panel-title>
                                                <v-btn
                                                    class="text-none text-subtitle-1"
                                                    size="small"
                                                    variant="flat"
                                                    @click.stop="choix(index)"
                                                >
                                                    {{ uo.nom }}
                                                </v-btn>                                                
                                            </v-expansion-panel-title>
                                            <v-expansion-panel-text>
                                                <!-- Niveau 2 services -->
                                                <div v-for="(uo, index) in uo.enfants" :key="index">
                                                    <div v-if="uo.enfants.length === 0">
                                                        <span class="spnalign"></span>
                                                        <v-btn
                                                            class="text-none text-subtitle-1"
                                                            size="small"
                                                            variant="flat"
                                                            @click.stop="choix(index)"
                                                        >
                                                            {{ uo.nom }}
                                                        </v-btn>                                                
                                                    </div>    
                                                    <div v-else>
                                                        <v-expansion-panels>
                                                            <v-expansion-panel>
                                                                <v-expansion-panel-title>
                                                                    <v-btn
                                                                        class="text-none text-subtitle-1"
                                                                        size="small"
                                                                        variant="flat"
                                                                        @click.stop="choix(index)"
                                                                    >
                                                                        {{ uo.nom }}
                                                                    </v-btn>                                                
                                                                </v-expansion-panel-title>
                                                                <v-expansion-panel-text>
                                                                    <!-- Niveau 3 sous-services -->
                                                                    <div v-for="(uo, index) in uo.enfants" :key="index">
                                                                        <div v-if="uo.enfants.length === 0">
                                                                            <span class="spnalign"></span>
                                                                            <v-btn
                                                                                class="text-none text-subtitle-1"
                                                                                size="small"
                                                                                variant="flat"
                                                                                @click.stop="choix(index)"
                                                                            >
                                                                                {{ uo.nom }}
                                                                            </v-btn>                                                
                                                                        </div>    
                                                                        <div v-else>
                                                                            <v-expansion-panels>
                                                                                <v-expansion-panel>
                                                                                    <v-expansion-panel-title>
                                                                                        <v-btn
                                                                                            class="text-none text-subtitle-1"
                                                                                            size="small"
                                                                                            variant="flat"
                                                                                            @click.stop="choix(index)"
                                                                                        >
                                                                                            {{ uo.nom }}
                                                                                        </v-btn>                                                
                                                                                    </v-expansion-panel-title>
                                                                                    <v-expansion-panel-text>
                                                                                        <!-- Niveau 4 -->
                                                                                        <div v-for="(uo, index) in uo.enfants" :key="index">
                                                                                            <div v-if="uo.enfants.length === 0">
                                                                                                <span class="spnalign"></span>
                                                                                                <v-btn
                                                                                                    class="text-none text-subtitle-1"
                                                                                                    size="small"
                                                                                                    variant="flat"
                                                                                                    @click.stop="choix(index)"
                                                                                                >
                                                                                                    {{ uo.nom }}
                                                                                                </v-btn>                                                
                                                                                            </div>    
                                                                                            <div v-else>
                                                                                                <v-expansion-panels>
                                                                                                    <v-expansion-panel>
                                                                                                        <v-expansion-panel-title>
                                                                                                            <v-btn
                                                                                                                class="text-none text-subtitle-1"
                                                                                                                size="small"
                                                                                                                variant="flat"
                                                                                                                @click.stop="choix(index)"
                                                                                                            >
                                                                                                                {{ uo.nom }}
                                                                                                            </v-btn>                                                
                                                                                                        </v-expansion-panel-title>
                                                                                                        <v-expansion-panel-text>
                                                                                                            <!-- Niveau 5 -->
                                                                                                            <div v-for="(uo, index) in uo.enfants" :key="index">
                                                                                                                <div v-if="uo.enfants.length === 0">
                                                                                                                    <span class="spnalign"></span>
                                                                                                                    <v-btn
                                                                                                                        class="text-none text-subtitle-1"
                                                                                                                        size="small"
                                                                                                                        variant="flat"
                                                                                                                        @click.stop="choix(index)"
                                                                                                                    >
                                                                                                                        {{ uo.nom }}
                                                                                                                    </v-btn>                                                
                                                                                                                </div>    
                                                                                                                <div v-else>
                                                                                                                    <v-expansion-panels>
                                                                                                                        <v-expansion-panel>
                                                                                                                            <v-expansion-panel-title>
                                                                                                                                <v-btn
                                                                                                                                    class="text-none text-subtitle-1"
                                                                                                                                    size="small"
                                                                                                                                    variant="flat"
                                                                                                                                    @click.stop="choix(index)"
                                                                                                                                >
                                                                                                                                    {{ uo.nom }}
                                                                                                                                </v-btn>                                                
                                                                                                                            </v-expansion-panel-title>
                                                                                                                            <v-expansion-panel-text>
                                                                                                                                <!-- Niveau 6 -->
                                                                                                                                <div v-for="(uo, index) in uo.enfants" :key="index">
                                                                                                                                    <div v-if="uo.enfants.length === 0">
                                                                                                                                        <span class="spnalign"></span>
                                                                                                                                        <v-btn
                                                                                                                                            class="text-none text-subtitle-1"
                                                                                                                                            size="small"
                                                                                                                                            variant="flat"
                                                                                                                                            @click.stop="choix(index)"
                                                                                                                                        >
                                                                                                                                            {{ uo.nom }}
                                                                                                                                        </v-btn>                                                
                                                                                                                                    </div>    
                                                                                                                                    <div v-else>
                                                                                                                                        <v-expansion-panels>
                                                                                                                                            <v-expansion-panel>
                                                                                                                                                <v-expansion-panel-title>
                                                                                                                                                    <v-btn
                                                                                                                                                        class="text-none text-subtitle-1"
                                                                                                                                                        size="small"
                                                                                                                                                        variant="flat"
                                                                                                                                                        @click.stop="choix(index)"
                                                                                                                                                    >
                                                                                                                                                        {{ uo.nom }}
                                                                                                                                                    </v-btn>                                                
                                                                                                                                                </v-expansion-panel-title>
                                                                                                                                                <v-expansion-panel-text>
                                                                                                                                                <!-- Niveau 7 -->
                                                                                                                                                <div v-for="(uo, index) in uo.enfants" :key="index">
                                                                                                                                                    <div v-if="uo.enfants.length === 0">
                                                                                                                                                        <span class="spnalign"></span>
                                                                                                                                                        <v-btn
                                                                                                                                                            class="text-none text-subtitle-1"
                                                                                                                                                            size="small"
                                                                                                                                                            variant="flat"
                                                                                                                                                            @click.stop="choix(index)"
                                                                                                                                                        >
                                                                                                                                                            {{ uo.nom }}
                                                                                                                                                        </v-btn>                                                
                                                                                                                                                    </div>    
                                                                                                                                                    <div v-else>
                                                                                                                                                        <v-expansion-panels>
                                                                                                                                                            <v-expansion-panel>
                                                                                                                                                                <v-expansion-panel-title>
                                                                                                                                                                    <v-btn
                                                                                                                                                                        class="text-none text-subtitle-1"
                                                                                                                                                                        size="small"
                                                                                                                                                                        variant="flat"
                                                                                                                                                                        @click.stop="choix(index)"
                                                                                                                                                                    >
                                                                                                                                                                        {{ uo.nom }}
                                                                                                                                                                    </v-btn>                                                
                                                                                                                                                                </v-expansion-panel-title>
                                                                                                                                                                <v-expansion-panel-text>
                                                                                                                                                                <!-- Niveau 8 -->
                                                                                                                                                                <div v-for="(uo, index) in uo.enfants" :key="index">
                                                                                                                                                                    <div v-if="uo.enfants.length === 0">
                                                                                                                                                                        <span class="spnalign"></span>
                                                                                                                                                                        <v-btn
                                                                                                                                                                            class="text-none text-subtitle-1"
                                                                                                                                                                            size="small"
                                                                                                                                                                            variant="flat"
                                                                                                                                                                            @click.stop="choix(index)"
                                                                                                                                                                        >
                                                                                                                                                                            {{ uo.nom }}
                                                                                                                                                                        </v-btn>                                                
                                                                                                                                                                    </div>    
                                                                                                                                                                    <div v-else>
                                                                                                                                                                        <v-expansion-panels>
                                                                                                                                                                            <v-expansion-panel>
                                                                                                                                                                                <v-expansion-panel-title>
                                                                                                                                                                                    <v-btn
                                                                                                                                                                                        class="text-none text-subtitle-1"
                                                                                                                                                                                        size="small"
                                                                                                                                                                                        variant="flat"
                                                                                                                                                                                        @click.stop="choix(index)"
                                                                                                                                                                                    >
                                                                                                                                                                                        {{ uo.nom }}
                                                                                                                                                                                    </v-btn>                                                
                                                                                                                                                                                </v-expansion-panel-title>
                                                                                                                                                                                <v-expansion-panel-text>
                                                                                                                                                                                    !!! Niveau hiérarchique non traité, prévenir le support goéland !!!
                                                                                                                                                                                </v-expansion-panel-text>
                                                                                                                                                                            </v-expansion-panel>   
                                                                                                                                                                    </v-expansion-panels>
                                                                                                                                                                    </div>
                                                                                                                                                                </div>
                                                                                                                                                                </v-expansion-panel-text>
                                                                                                                                                            </v-expansion-panel>   
                                                                                                                                                    </v-expansion-panels>
                                                                                                                                                    </div>
                                                                                                                                                </div>
                                                                                                                                                </v-expansion-panel-text>
                                                                                                                                            </v-expansion-panel>   
                                                                                                                                    </v-expansion-panels>
                                                                                                                                    </div>
                                                                                                                                </div>
                                                                                                                           </v-expansion-panel-text>
                                                                                                                        </v-expansion-panel>   
                                                                                                                </v-expansion-panels>
                                                                                                                </div>
                                                                                                            </div>
                                                                                                        </v-expansion-panel-text>
                                                                                                    </v-expansion-panel>   
                                                                                            </v-expansion-panels>
                                                                                            </div>
                                                                                        </div>
                                                                                    </v-expansion-panel-text>
                                                                                </v-expansion-panel>   
                                                                        </v-expansion-panels>
                                                                        </div>
                                                                    </div>

                                                                </v-expansion-panel-text>
                                                            </v-expansion-panel>   
                                                    </v-expansion-panels>
                                                    </div>
                                                </div>
                                            </v-expansion-panel-text>
                                        </v-expansion-panel>   
                                </v-expansion-panels>
                                </div>
                            </div>
                        </v-expansion-panel-text>
                    </v-expansion-panel>   
                </v-expansion-panels>
            </v-col>
        </v-row>
    </v-container>

</template>
  
  <script setup>
  import { ref } from 'vue'

  const panelN0 = ref([0])
  const panelN1 = ref([])
    
  const unitesOrg = 
    {
      nom: 'Ville de Lausanne',
      enfants: [
            {
                nom:'Direction 1',
                enfants: [
                    {
                        nom: 'Service 1-1',
                        enfants: [
                            {
                                nom: 'Goéland',
                                enfants: [
                                    {
                                    nom: 'Goéland Dev Team',
                                    enfants: []
                                }

                                ]
                            }
                        ],
                    },
                    {
                        nom: 'Service 1-2',
                        enfants: [
                            {
                                nom: 'Niveau 3 a',
                                enfants: [
                                    
                                ],
                            },
                            {
                                nom: 'Niveau 3 b',
                                enfants: [
                                    {
                                        nom: 'Niveau 4 a',
                                        enfants: [
                                            
                                        ],
                                    },
                                    {
                                        nom: 'Niveau 4 b',
                                        enfants: [
                                            {
                                                nom: 'Niveau 5 a',
                                                enfants: [
                                                    
                                                ],
                                            },
                                            {
                                                nom: 'Niveau 5 b',
                                                enfants: [
                                                    
                                                ],
                                            }
                                        ],
                                    }
                                    
                                ],
                            }


                        ],
                    }
                ]
            }, 
            {
                nom:'Direction 2',
                enfants: [
                    {
                        nom: 'Service 2-1',
                        enfants: [],
                    },
                    {
                        nom: 'Service 2-2',
                        enfants: [],
                    }
                ]
            }, 
      ]
    }

    const choix = (i) => {
        console.log('choix: ' + i)
    }    
  </script>