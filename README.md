# Azimute

**Azimute: Automação da leitura de matrículas para conversão de dados cartorários em inteligência geográfica e atualização da base imobiliária fiscal.**

Este projeto foi desenvolvido no âmbito da **DIMAP (Divisão do Mapa de Valores)**, unidade da **Secretaria Municipal da Fazenda de São Paulo**. O objetivo principal é otimizar o fluxo de processamento de informações imobiliárias, transformando registros analógicos e desestruturados em dados acionáveis para a administração tributária.

## Contexto e Valor

O Azimute resolve o desafio técnico de extrair e espacializar dados de matrículas de imóveis. No contexto da Secretaria da Fazenda, isso se traduz em:

- Atualização da Base Imobiliária Fiscal: Sincronização automática entre os registros de cartório e o cadastro municipal.
- Inteligência Geográfica: Conversão de descrições textuais e coordenadas em perímetros auditáveis.
- Justiça Fiscal: Garantia de que a tributação reflita a realidade física e jurídica do território.

## Arquitetura do Sistema

O projeto adota uma arquitetura inspirada no padrão Hexagonal (Ports and Adapters), organizada por domínios funcionais para garantir manutenibilidade e escalabilidade:

- Domain Layer: Contém o núcleo da lógica de negócio, protocolos e serviços de orquestração, totalmente independentes de frameworks externos.
- Infrastructure Layer: Implementa os adapters para bibliotecas específicas (como PyMuPDF para extração nativa e futuros módulos de OCR).
- API Layer: Interface baseada em Django Ninja, estruturada em roteadores modulares por domínio.

## Stack Tecnológica

- Linguagem: Python 3.10+
- Web Framework: Django com Django Ninja (FastAPI-style)
- PDF Engine: PyMuPDF (fitz)
- Geoprocessamento: Shapely e PyProj (em fase de planejamento)
- Frontend: HTMX e Tailwind CSS / DaisyUI (para interface administrativa interna)

## Status do Projeto

Atualmente, o projeto encontra-se em fase de MVP, focado na extração automatizada de textos de PDFs nativos. O roadmap inclui o desenvolvimento do parser de geometria para reconstrução de perímetros a partir de azimutes e confrontantes.

---
Desenvolvido pela equipe técnica da DIMAP - Secretaria da Fazenda.
