---
title: Správa poruch
description: Tento článek popisuje správu poruch v modulu Správa majetku.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetFaultArea, EntAssetFaultDesigner, EntAssetFaultCopyFromObjectType, EntAssetFaultRemedy, EntAssetObjectFaultRelationRequestInfoPart, EntAssetObjectFaultRelationWorkOrderInfoPart, EntAssetFaultCreateCombinations, EntAssetObjectFaultSymptom, EntAssetObjectFaultSymptomListPage, EntAssetFaultType, EntAssetFaultSymptom, EntAssetFaultCause
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 10a4a209b54aa31c4a2f6970f46ab8b1a2cbef97
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874152"
---
# <a name="fault-management"></a>Správa poruch

[!include [banner](../../includes/banner.md)]

 

V modulu Správa majetku můžete pomocí Návrháře poruch nastavit příznaky poruch, oblasti poruch a typy poruch na typech majetku. Tímto způsobem lze spravovat poruchy zjištěné u majetku. Kromě toho mohou být v rámci pracovního příkazu registrovány příčiny poruch a návrhy na jejich opravu.

Proces registrace a správy poruch sestává z těchto kroků.

1. Vytvořte seznam příznaků poruch, oblastí poruch a typů poruch, které mohou nastat u vašich typů majetku.
2. V Návrháři poruch nastavte příznaky, oblasti poruch a typy poruch.

Zde jsou uvedeny některé příklady, které vám pomohou pochopit rozdíly mezi příznaky poruch, oblastmi poruch a typy poruch.

**Příznaky poruch:**

- Nevyrovnané elektrické napětí
- Krátký obvod
- Hluk
- Únik kapaliny
- Vibrace

**Oblasti poruch:**

- Elektrická
- Mechanická
- Hydraulická
- Pneumatická

**Typy poruch:**

- Chybné hlavní vinutí statoru
- Vadná dioda
- Znečištěné vinutí
- Chybný generátor
- Vadný senzor

## <a name="create-fault-symptoms"></a>Vytvoření příznaků poruch

Pomocí následujících kroků vytvořte seznam příznaků, které lze použít v Návrháři poruch.

1. Vyberte **Správa majetku** \> **Nastavení** \> **Porucha** \> **Příznaky poruch**.
2. Zvolte **Nový** pro vytvoření záznamu.
3. Do pole **Příznak poruchy** zadejte název příznaku poruchy.
4. Zadejte popis do pole **Popis**.
5. Zvolte **Uložit**.

## <a name="create-fault-areas"></a>Vytvoření oblastí poruch

Pomocí následujících kroků vytvořte oblasti poruch, které lze použít v Návrháři poruch.

1. Vyberte **Správa majetku** \> **Nastavení** \> **Porucha** \> **Oblasti poruch**.
2. Zvolte **Nový** pro vytvoření záznamu.
3. Do pole **Oblast poruchy** zadejte název oblasti poruchy.
4. Zadejte popis do pole **Popis**.
5. Zvolte **Uložit**.

## <a name="create-fault-types"></a>Vytvoření typů poruch

Pomocí následujících kroků vytvořte seznam typů poruch, které lze použít v Návrháři poruch.

1. Vyberte **Správa majetku** \> **Nastavení** \> **Porucha** \> **Typy poruch**.
2. Zvolte **Nový** pro vytvoření záznamu.
3. Do pole **Typ poruchy** zadejte název typu poruchy.
4. Zadejte popis do pole **Popis**.
5. Zvolte **Uložit**.

## <a name="set-up-the-fault-designer"></a>Nastavení Návrháře poruch

V Návrháři poruch se nastavují údaje o poruchách pro typy majetku.

1. Vyberte **Správa majetku** \> **Nastavení** \> **Porucha** \> **Návrhář poruch**.
2. V levém podokně vyberte typ majetku, pro který chcete nastavit záznam poruchy.
3. Na záložce s náhledem **Příznak poruchy** vyberte možnost **Přidat řádek** a poté v poli **Příznak poruchy** vyberte příznak poruchy.
4. Na záložce s náhledem **Oblast poruchy** vyberte možnost **Přidat řádek** a poté v poli **Oblast poruchy** vyberte oblast poruchy.
5. Na záložce s náhledem **Typ poruchy** vyberte možnost **Přidat řádek** a poté v poli **Typ poruchy** vyberte typ poruchy.
6. Chcete-li rychle vytvořit kombinace všech existujících příznaků, oblastí a typů poruch pro vybraný typ majetku, vyberte možnost **Vytvořit kombinace poruch**. Tato funkce je užitečná v případě, že jste přidali mnoho příznaků, oblastí a typů poruch. Je jednodušší odstranit řádky pro všechny kombinace, které nesouvisejí s typem majetku, než vytvářet nové řádky ručně.

    > [!NOTE]
    > Chcete-li zkopírovat nastavení příznaků, oblastí a typů poruch z jednoho typu majetku na vybraný typ majetku, vyberte možnost **Kopírovat z typu majetku**.

7. Klepnutím na tlačítko **Uložit** uložte změny.

![Stránka návrháře chyb.](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a>Vytvoření příčin poruch

Chcete-li vytvořit seznam známých příčin poruch, které lze přidat na pracovní příkaz nebo požadavek na údržbu, postupujte podle následujících kroků.

1. Vyberte **Správa majetku** \> **Nastavení** \> **Porucha** \> **Příčiny poruch**.
2. Zvolte **Nový** pro vytvoření záznamu.
3. Do pole **Příčina poruchy** zadejte název příčiny poruchy.
4. Zadejte popis do pole **Popis**.
5. Zvolte **Uložit**.

## <a name="create-fault-remedies"></a>Vytvoření náprav poruch

Chcete-li vytvořit seznam navrhovaných náprav a oprav, které lze přidat na pracovní příkaz nebo požadavek na údržbu, postupujte podle následujících kroků.

1. Vyberte **Správa majetku** \> **Nastavení** \> **Porucha** \> **Náprava poruch**.
2. Zvolte **Nový** pro vytvoření záznamu.
3. Do pole **Náprava poruchy** zadejte název nápravy poruchy.
4. Zadejte popis do pole **Popis**.
5. Zvolte **Uložit**.

> [!NOTE]
> Podle potřeby můžete změnit názvy příznaků, oblastí, typů, příčin a náprav poruch. Změny názvu se automaticky projeví v souvisejících registracích poruch.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]