---
title: Nastavení a spuštění zpracování pro volání jednoduchého formátu elektronického výkaznictví pro vygenerování sestavy v aplikaci Excel
description: Tento článek poskytuje příklad, který ukazuje, jak nastavit a používat elektronické zprávy.
author: AdamTrukawka
ms.date: 07/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.21
ms.custom: ''
ms.search.form: ''
ms.openlocfilehash: 6090c45a98b672f718f89fc1d2e1c060498bb8a0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279327"
---
# <a name="set-up-and-run-processing-to-call-a-simple-exporting-er-format-to-generate-an-excel-report"></a>Nastavení a spuštění zpracování pro volání jednoduchého formátu elektronického výkaznictví pro vygenerování sestavy v aplikaci Excel

[!include [banner](../includes/banner.md)]

Po vytvoření formátu elektronického výkaznictví, jeho namapování na datové zdroje jeho dokončení ho můžete spustit z pracovního prostoru **Elektronické výkaznictví**. Po vygenerování můžete sestavu uložit místně.

Chcete-li řídit následující aspekty procesu vykazování, nastavte zpracování elektronických zpráv:

- Zaprotokolování informací o tom, kdo vygeneroval sestavu.
- Zaprotokolujte informace o tom, kdo vygeneroval sestavu.
- Uložte sestavy, které byly vygenerovány za předchozí období.

Následující příklad ukazuje, jak můžete nastavit elektronické zprávy a vygenerovat sestavu založenou na formátu exportu elektronického výkaznictví pro aplikaci Microsoft Excel. Pokud chcete postupovat podle tohoto příkladu, formát exportu elektronického výkaznictví v Excelu musí být již vytvořen, namapován na zdroje dat a dokončen. Dále platí, že číselná řada již musí být nastavena pro elektronické zprávy.

Při vytváření zpracování je užitečné, pokud nejprve definujete akce a stavy zpracování, které budou vytvořeny. Následující obrázek znázorňuje zpracování v tomto příkladu.

![Schéma zpracování](media/processing-scheme.png)

## <a name="create-message-statuses"></a>Vytvoření stavů zpráv

1. Přejděte na **Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Stavy zprávy**.
2. Vytvořte následující stavy zprávy:

    - Nová
    - Připraveno
    - Vytvořeno

    ![Stavy zpráv](media/message-statuses.png)

3. Na řádku stavu **Nový** vyberte zaškrtávací políčko **Povolit odstranění** a umožněte uživatelům odstranit zprávy s tímto stavem.

## <a name="create-additional-fields"></a>Vytvoření dalších polí

1. Přejděte na **Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Další pole**.
2. Přidejte další pole a jeho hodnoty.
3. Nastavte možnost **Úpravy uživatele** na **Ano**, čímž umožníte uživatelům upravit pole.

![Dodatečná pole](media/additional-fields.png)

## <a name="create-message-processing-actions"></a>Vytvoření akcí zpracování zprávy

V tomto příkladu vytvoříte následující akce zpracování zpráv:

- **Vytvořit zprávu**
- **Aktualizovat na Připraveno**
- **Generovat sestavu**
- **Aktualizovat na počáteční stav** (volitelné)

Při vytváření akcí postupujte takto.

1. Přejděte na **Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Akce zpracování zprávy**.
2. Vytvořte akci, která se nazývá **Vytvořit zprávu**. Na záložce s náhledem **Obecné** v poli **Typ akce** vyberte **Vytvořit zprávu**.
3. Vytvořte akci, která se nazývá **Aktualizovat na Připraveno** a nastavte následující pole:

    - Na záložce s náhledem **Obecné** v poli **Typ akce** vyberte **Zpracování uživatele na úrovni zprávy**.
    - Na záložce s náhledem **Počáteční stavy** v poli **Stav zprávy** vyberte **Nový**.
    - Na záložce s náhledem **Výsledné stavy** v poli **Stav zprávy** vyberte **Připraveno**. V poli **Typ odezvy** zadejte **Úspěšně provedeno**.

4. Vytvořte akci, která se nazývá **Generovat sestavu** a nastavte následující pole:

    - Na záložce s náhledem **Obecné** v poli **Typ akce** vyberte **Export elektronického výkaznictví**. V poli **Mapování formátu** vyberte formát exportu elektronického výkaznictví. Možnosti jsou **Excel**, **XML**, **JSON**, **Text** a **Jiné**.
    - Na záložce s náhledem **Počáteční stavy** v poli **Stav zprávy** vyberte **Připraveno**.
    - Na záložce s náhledem **Výsledné stavy** v poli **Stav zprávy** vyberte **Vygenerováno**. V poli **Typ odezvy** zadejte **Úspěšně provedeno**.

    ![Generování akce sestavy](media/generate-report-action.png)

5. Volitelné: Abyste umožnili uživatelům vygenerovat sestavu několikrát, vytvořte akci s názvem **Aktualizovat na počáteční stavu** a nastavte následující pole:

    - Na záložce s náhledem **Obecné** v poli **Typ akce** vyberte **Zpracování uživatele na úrovni zprávy**.
    - Na záložce s náhledem **Počáteční stavy** v poli **Stav zprávy** vyberte **Vygenerováno**.
    - Na pevné záložce **Výsledně stavy** přidejte samostatný řádek pro každý ze dvou stavů zprávy (**Připraveno** a **Nový**). Pro oba řádky nastavte pole **typ odezvy** na **úspěšně spuštěno**.

## <a name="electronic-message-processing"></a>Zpracování elektronické zprávy

V tomto příkladu by všechny akce měly být nastaveny tak, aby se spouštěly samostatně. Předpokladem je, že každá akce bude inicializována uživatelem.

1. Přejděte na **Daň** \> **Nastavení** \> **Elektronické zprávy** \> **Zpracování elektronické zprávy**.
2. Přidejte záznam pro zpracování a přidejte všechny dříve definované akce a další pole.
3. Volitelné: Na záložce s náhledem **Role zabezpečení** definujte role zabezpečení pro vaše zpracování, abyste omezili přístup ke konkrétnímu vykazování.
4. Přejděte na **Daň** \> **Dotazy a sestavy** \> **Elektronické zprávy** \> **Elektronické zprávy**.
5. Zvolte **Nová** pro vytvoření zprávy. Nyní můžete přidat data a popis. Můžete také aktualizovat hodnotu dalšího pole podle potřeby.

    ![Vytvoření elektronické zprávy](media/create-electronic-message.png)

    Mřížka na záložce s náhledem **Protokol akce** je automaticky vyplněna protokolem všech akcí, které jsou provedeny na zprávě.

    Nyní můžete odstranit nebo aktualizovat stav zprávy. 

6. Chcete-li aktualizovat stav zprávy, vyberte **Aktualizovat stav**. V poli **nový stav** vyberte **Připraveno** a poté vyberte **OK**.

    ![Aktualizace stavu zprávy](media/update-status.png)

    Stav zprávy je aktualizován na **Připravená**.

7. Vytvořte sestavu výběrem **Generovat sestavu**.

    Sestava se vygeneruje a aktualizuje se stav zprávy a protokol akce.

8. Chcete-li zobrazit generovanou sestavu, vyberte tlačítko **Příloha** (ikona papírové svorky) v pravém horním rohu stránky.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
