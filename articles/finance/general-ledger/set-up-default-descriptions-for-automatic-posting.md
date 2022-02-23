---
title: Nastavení výchozích popisů pro automatické zaúčtování
description: Toto téma popisuje jak nastavit výchozí text, který se používá k popisu účetních zápisů, které jsou automaticky zaúčtovány do hlavní knihy. Můžete nastavit výchozí text s popisem pomocí volného textu nebo výběrem pevných proměnných.
author: aprilolson
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f5fc73f636a5cac25c259ce2cbae5c5407dca9b7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440988"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a>Nastavení výchozích popisů pro automatické zaúčtování

[!include [banner](../includes/banner.md)]

Toto téma popisuje jak nastavit výchozí text, který se používá k popisu účetních zápisů, které jsou automaticky zaúčtovány do hlavní knihy. Můžete nastavit výchozí text s popisem pomocí volného textu nebo výběrem pevných proměnných.

> [!NOTE]
> U některých typů transakcí v některých zemích/oblastech lze také vložit text z polí do databáze aplikace Microsoft Dynamics AX, která se vztahuje na tyto typy transakcí. Seznam typů transakcí a zemí a oblastí naleznete v části [Volitelné: Přídání dalšího textu do výchozího popisu](#optional-add-other-text-to-default-descriptions) dále v tomto tématu.

## <a name="set-up-default-descriptions"></a>Nastavit výchozí popisy

1. Přejděte do nabídky **Správa organizace** \> **Nastavení** \> **Výchozí popisy**.
2. V podokně akcí zvolte **Nový**.
3. Vyberte v poli **Popis** typ transakce, pro který chcete vytvořit výchozí popis.
4. Vyberte v poli **Jazyk** požadovaný jazyk, který odpovídá tomuto popisu.
5. Zadejte do pole **Text** výchozí popis. V tomto poli můžete zadat text nebo můžete použít jeden nebo více následujících proměnných s volným textem:

    - **%1** – Přidejte datum transakce.
    - **%2** – Přidejte identifikátor odpovídající typu dokumentu, který má být zaúčtován do hlavní knihy. Například pro typy transakcí, které se vztahují k fakturám, proměnná **%2** přidává číslo faktury.
    - **%3** – Přidá identifikátor vztahující se k typu dokumentu, který má být zaúčtován do hlavní knihy. Například pro typy transakcí, které se vztahují k fakturám, proměnná **%3** přidává číslo účtu zákazníka.

## <a name="optional-add-other-text-to-default-descriptions"></a>Volitelné: Přidání dalšího textu do výchozích popisů

U některých typů transakcí v některých zemích/oblastech mohou výchozí popisy obsahovat text, který pochází z polí do databáze aplikace , která se vztahuje na tyto typy transakcí. Tyto seznamy ukazují typy transakcí a země a oblasti, pro které je tato možnost k dispozici.

**Typy transakcí**

Můžete přidat jiný text do výchozích popisů pro typy transakcí, které souvisejí s následujícími typy dokumentů:

- Faktury odběratele
- Dobropisy zákazníkům
- Platby hotovosti zákazníkům
- Platby dodavatelů
- Prodejní objednávky
- Nákupní objednávky
- Skladové deníky
- Hlavní plánování (MRP)
- Dlouhodobý majetek

**Země a oblasti**

Tato možnost je k dispozici pro následující země či oblasti:

- Brazílie
- Čína
- Česká republika
- Východní Evropa
- Maďarsko
- Indie
- Japonsko
- Litva
- Lotyšsko
- Polsko
- Rusko

### <a name="add-text-to-default-descriptions"></a>Přidání dalšího textu do výchozích popisů

Po dokončení kroků uvedených v části [Nastavení výchozích popisů](#set-up-default-descriptions) dříve v tomto tématu postupujte takto pro přidání dalšího textu do výchozích popisů.

1. Na pevné záložce **Parametry** vyberte **Přidat**.
2. V poli **Referenční tabulka** vyberte tabulku databáze, ze které chcete přidat data parametru do popisu.
3. V poli **Referenční pole** vyberte pole databáze, ze kterého chcete přidat data parametru do popisu.
4. Opakováním kroků 1 až 3 přidejte další parametry.
