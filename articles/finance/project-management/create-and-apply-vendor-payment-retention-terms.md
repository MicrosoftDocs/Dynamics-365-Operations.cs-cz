---
title: Vytvoření a použití podmínek zadržení plateb dodavateli
description: Toto téma obsahuje informace o tom, jak nastavit a udržovat podmínky zadržení plateb dodavatelům.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 0e14050a79220b5d02763a025040edb934489d00
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410201"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Vytvoření a použití podmínek zadržení plateb dodavateli

[!include [banner](../includes/banner.md)] 

Nastavení podmínek zadržení plateb dodavateli pro projekt je užitečné, pokud si vaše organizace přeje ponechat část plateb provedených některému dodavateli. Například pokud chcete pozastavit platbu dodavateli, dokud dodané produkty nesplní vaše očekávání. Podmínky zadržení platby dodavateli lze upřesnit, když vyjednáváte smlouvu s dodavatelem.

## <a name="create-vendor-payment-retention-terms"></a>Vytvoření podmínek zadržení platby dodavateli

Můžete zadat procento zadržené platby dodavateli a procento dříve zadržené částky, kterou chcete vydat. Částky jsou automaticky zachovány na faktuře dodavateli, dokud smlouva nedosáhne určeného stavu dokončení. Po nastavení podmínek zadržení je můžete použít pro jakýkoli projekt tohoto dodavatele.

Pomocí následujícího postupu můžete nastavit a spravovat podmínky zadržení plateb dodavatelům. 

1. Přejděte na **Řízení projektů a účetnictví** > **Zadržení** > **Podmínky zadržení plateb dodavateli**.
2. Volbou **Nová** přidáte nové podmínky zadržení platby dodavateli. Automaticky se zadá hodnota **ID pravidla** pro novou podmínku. 
3. Do pole **Popis** zadejte krátký popis a na záložce s náhledem **Podmínky** volbou **Přidat řádek** zadejte hodnoty podmínek pro následující:

   - **Procento dodaných jednotek**: Zadejte procento dokončení pro daný termín. Na faktuře dodavatele se částka automaticky zachová, dokud není fáze dokončení projektu rovna zadanému procentu. Například pokud zadáte hodnotu 50,00, částky budou zachovány, dokud nebude projekt dokončen z 50 procent.
   - **Procento k zadržení**: Zadejte procento zadržené částky faktury dodavatele. Například pokud zadáte hodnotu 10,00, 10 procent z částky na faktuře dodavatele na zůstane zachováno až dokud projektu nedosáhne procenta dokončení zadaného v poli **Procento dodaných jednotek**.
   - **Procento k uvolnění**: Volbou **Přidat řádek** zadejte procento libovolné dříve zachované částky, kterou chcete vydat po dosažení vybrané úrovně dokončení projektu.

> [!NOTE]
> Pokud máte více než jeden milník pro různé úrovně dokončení projektu, zadejte samostatný řádek s retenčními podmínky dodavateli pro každé retenční pravidlo. Každý řádek můžete představovat jiné procento zadržení a uvolnění pro každou uvedenou úroveň dokončení projektu.

Po vytvoření podmínek zadržení platby dodavateli je můžete použít na projekt.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Použití podmínek zadržení platby dodavateli na projekt

1. Přejděte na **Řízení projektů a účetnictví** > **Projekty** > **Všechny projekty** a otevřete projekt ze stránky seznamu projektů.
2. Na pevné kartě **Smlouvy s dodavatelem** vyberte tlačítko **Přidat řádek**.
3. V poli **Kód účtu** vyberte jednu z následujících možností: 

   - **Tabulka**: Podmínky zadržení platby dodavateli se vztahují na jednoho dodavatele.
   - **Skupina**: Podmínky zadržení platby dodavateli se vztahují na všechny dodavatele ve skupině dodavatelů.
   - **Vše**: Podmínky zadržení platby dodavateli se vztahují na všechny dodavatele.

4. V poli **Dodavatel/ skupina dodavatelů** vyberte dodavatele nebo skupinu dodavatelů, na kterou se vztahují podmínky zadržení platby dodavateli. Pokud jste v rámci předchozího kroku vybrali možnost **Vše**, toto pole nebude k dispozici.
5. V poli **Podmínky zádržného dodavatele** vyberte podmínky zádržného, které jste vytvořili v předchozích krocích.
6. Pokud projekt u daného dodavatele využívá také podmínky zaplacení po zaplacení (ZPZ), v poli **Procento prahu ZPZ** zadejte procentuální prahovou hodnotu pro projekt.

Retenční podmínky dodavateli se také zobrazují na nákupních objednávkách vytvořených pro dodavatele.
