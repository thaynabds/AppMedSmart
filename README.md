# AppMedSmart
Projeto de criação de protótipo de aplicativo para simplificação de receitas médicas
# MedSmart

O MedSmart é uma aplicação desenvolvida para atuar como um assistente inteligente na gestão de saúde, focado principalmente na organização e no cumprimento de cronogramas de medicação. O projeto visa proporcionar mais segurança e autonomia para pacientes que precisam lidar com rotinas de tratamento complexas.

## Funcionalidades Principais

* **Gerenciamento de Medicamentos:** Cadastro detalhado de remédios, incluindo dosagens e horários específicos.
* **Sistema de Alertas:** Notificações automáticas para garantir que o usuário tome a medicação no momento correto.
* **Histórico de Adesão:** Registro das doses tomadas para acompanhamento da evolução do tratamento e monitoramento de esquecimentos.
* **Interface Simplificada:** Design focado na experiência do usuário, garantindo que a navegação seja acessível e intuitiva.

## Objetivo do Projeto

O objetivo central do MedSmart é reduzir os riscos associados à administração incorreta de medicamentos, centralizando informações essenciais de saúde em uma única plataforma digital e auxiliando o usuário na manutenção de seus hábitos de cuidado pessoal.

[Demonstração do Protótipo (Figma)](https://www.figma.com/make/MsNZkHpprtDGEdfiXkXYav/App-MedSmart-2025-Prot%C3%B3tipo-?fullscreen=1&t=VDjT0wEL2rVxA1xR-1)

Neste  Link podemos ver o protótipo com funcionamento de interfaces para gestão de remédios, servindo como referência visual para o fluxo de notificações e cadastro proposto pelo MedSmart.

✒️ Autor [Thayná Batista da Silva](https://github.com/thaynabds) - Desenvolvimento e Design


---

## 2. Código Estrutural do App (Boilerplate)
Como o Figma não gera o código funcional completo, criei a estrutura básica da **Tela Principal (Dashboard)** em React Native para você começar a codificar a lógica:

```javascript
// App.js (Exemplo de estrutura base para o MedSmart)
import React from 'react';
import { StyleSheet, Text, View, ScrollView, TouchableOpacity } from 'react-native';
import { Ionicons } from '@expo/vector-icons';

export default function App() {
  return (
    <View style={styles.container}>
      {/* Header */}
      <View style={styles.header}>
        <Text style={styles.greeting}>Olá, Paciente</Text>
        <Text style={styles.subtitle}>Sua saúde está 85% monitorada hoje.</Text>
      </View>

      <ScrollView style={styles.content}>
        {/* Card de Próximo Remédio */}
        <View style={styles.card}>
          <Ionicons name="medical" size={32} color="#2D9CDB" />
          <View style={styles.cardText}>
            <Text style={styles.cardTitle}>Próximo Medicamento</Text>
            <Text style={styles.cardInfo}>Amoxicilina - 12:00h</Text>
          </View>
        </View>

        {/* Grade de Atalhos */}
        <View style={styles.grid}>
          <TouchableOpacity style={styles.menuItem}>
            <Ionicons name="calendar" size={24} color="#fff" />
            <Text style={styles.menuText}>Agenda</Text>
          </TouchableOpacity>
          <TouchableOpacity style={[styles.menuItem, {backgroundColor: '#27AE60'}]}>
            <Ionicons name="pulse" size={24} color="#fff" />
            <Text style={styles.menuText}>Sinais</Text>
          </TouchableOpacity>
        </View>
      </ScrollView>
    </View>
  );
}

const styles = StyleSheet.create({
  container: { flex: 1, backgroundColor: '#F5F5F5' },
  header: { padding: 30, paddingTop: 60, backgroundColor: '#2D9CDB' },
  greeting: { fontSize: 24, fontWeight: 'bold', color: '#fff' },
  subtitle: { color: '#E0E0E0', marginTop: 5 },
  content: { padding: 20 },
  card: { 
    backgroundColor: '#fff', padding: 20, borderRadius: 15, 
    flexDirection: 'row', alignItems: 'center', elevation: 3 
  },
  cardText: { marginLeft: 15 },
  cardTitle: { fontWeight: 'bold', fontSize: 16 },
  grid: { flexDirection: 'row', justifyContent: 'space-between', marginTop: 20 },
  menuItem: { 
    backgroundColor: '#2D9CDB', width: '48%', height: 100, 
    borderRadius: 15, justifyContent: 'center', alignItems: 'center' 
  },
  menuText: { color: '#fff', marginTop: 8, fontWeight: '500' }
});
