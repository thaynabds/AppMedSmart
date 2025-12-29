Aqui está a versão atualizada do seu README, incluindo a observação de que o projeto é um protótipo em desenvolvimento, mantendo a fidelidade total aos links e informações fornecidas:

💊 MedSmart
O MedSmart é uma aplicação desenvolvida para atuar como um assistente inteligente na gestão de saúde, focado na simplificação de receitas médicas e na organização de cronogramas de medicação. O projeto visa proporcionar mais segurança e autonomia para pacientes com rotinas de tratamento complexas.

⚠️ Status do Projeto: Protótipo em Desenvolvimento
O MedSmart encontra-se atualmente em fase de prototipagem e desenvolvimento inicial. As funcionalidades descritas fazem parte da visão do produto e estão sendo implementadas.

🎯 Objetivo
Reduzir os riscos associados à administração incorreta de medicamentos, centralizando informações essenciais de saúde em uma única plataforma digital e auxiliando o usuário na manutenção de seus hábitos de cuidado pessoal.

🚀 Funcionalidades Planejadas
Gerenciamento de Medicamentos: Cadastro detalhado de remédios, incluindo dosagens e horários específicos.

Sistema de Alertas: Notificações automáticas para garantir a pontualidade das doses.

Histórico de Adesão: Registro das doses tomadas para acompanhamento da evolução do tratamento e monitoramento de esquecimentos.

Monitoramento de Sinais: Acompanhamento de indicadores de saúde (como sinais vitais).

Interface Simplificada: Design intuitivo focado na acessibilidade e facilidade de navegação.

🎨 Design e Navegação
O fluxo visual e a interface do usuário podem ser explorados através do protótipo interativo abaixo:

🔗 Demonstração do Protótipo (Figma)

💻 Estrutura Técnica (Boilerplate)
Como parte do processo de desenvolvimento, aqui está a estrutura básica da Tela Principal (Dashboard) em React Native:

JavaScript

// App.js (Estrutura base para o MedSmart)
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
✒️ Autor
Thayná Batista da Silva - GitHub (Desenvolvimento e Design)
