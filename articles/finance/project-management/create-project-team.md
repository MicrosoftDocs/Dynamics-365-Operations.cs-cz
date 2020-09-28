---
title: Vytvoření projektového týmu
description: Tohle téma obsahuje informace, jak vytvořit a spravovat projektové týmy.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 834a6c0a4fcc32a955c1feddf0a6cbbb1f16b869
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760494"
---
# <a name="create-a-project-team"></a>Vytvoření projektového týmu

[!include [banner](../includes/banner.md)]

Pokud chcete použít role, které byly dříve nastaveny, v projektu, projektový manažer musí přiřadit role k projektu. Projektu může být přiřazeno více rolí. Aby se zabránilo nejasnostem, aplikace automaticky označuje tyto role během rezervace. Například pokud manažer projektu požaduje tři softwarové techniky, automaticky se vygenerují tři role softwarový technik, které jsou pojmenovány jako **Softwarový technik 1**, **Softwarový technik 2** a **Softwarový technik 3**. Pokud byly dříve pro roli nastaveny charakteristiky role, jsou použity jako filtr při hledání zdroje. Pro další upřesnění hledání lze volitelně přidat další charakteristiky.

Možnost Zobrazit nastavení lze také upravit tak, aby poskytovala lepší pohled na dostupnost prostředků. K dispozici je možnost zobrazit dostupnost hodinově, denně, týdně, měsíčně, čtvrtletně a ročně. Existuje také možnost zobrazit dostupnou a zbývající kapacitu prostředků. Tato možnost je užitečná pro časovou správu, pokud odhadujete dostupný čas pro aktivity nebo dostupnost prostředku.

Manažer projektu může vybrat roli na stránce a poté, je-li dostupný prostředek, který odpovídá požadavkům, může vybrat a rezervovat prostředek pro obsazení role. Mějte na paměti, že zdroje nemusí být v této fázi plánování rezervovány. Při vytváření struktury WBS můžete nahradit role skutečnými personálními prostředky pro daný projekt. Pokud role budou nahrazeny skutečnými zaměstnanci ve struktuře WBS, nastavení prostředků automaticky aktualizuje výpis a plánování projektového týmu.

[![Seznam týmů projektu, který obsahuje role a skutečné zdroje](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Vedoucí projektu má řadu možností pro rezervaci zdroje na projekt, například **Zbývající kapacita**, **Plná kapacita**, **Procento kapacity** a **Zadání hodin**. Tyto možnosti rezervace lze kdykoli zrušit v případě, že se změní přiřazení prostředků. Podporovány jsou dva typy rezervace:

- **Závazná rezervace** – Rezervace prostředku byla schválena a práce na projektu byla po určenou dobu trvání potvrzena.
- **Předběžná rezervace** – rezervace prostředku a účast na projektu po určenou dobu trvání je nezávazně schválena.

Při vytváření projektového týmu postupujte následujícím způsobem.

## <a name="create-a-project-team"></a>Vytvoření projektového týmu

1. Na stránce se seznamem **Všechny projekty** vyberte projekt a pak vyberte **Upravit**.
2. Na kartě **Projektový tým a plánování** v poli **Naplánovat koncové datum** zadejte datum zahájení plánu posunuté o jeden měsíc. Je-li datum zahájení plánu například 24. června 2017 (24/06/2017), zadejte **24/07/2017**.
3. Vyberte **přidat**.
4. V podokně **Přidat role do projektu** v poli **Role** vyberte **Vrchní manažer projektu**.
5. Vyberte **Požadované kompetence**.
6. Na stránce **Vybrat charakteristiky** jsou standardně zvoleny charakteristiky, které jste dříve nastavili pro roli Vrchní manažer projektu. Vyberte **OK**.
7. Na stránce **Přidat role do projektu** v poli **Počet prostředků** zadejte **1**.
8. V poli **Prostředek** vyhledávání zobrazí všechny zdroje, které mají požadované kompetence. Vyberte **Daniel Goldschmidt** a vyberte **Vytvořit**.
9. Na stránce **Projekt** vyberte **Přidat**.
10. V podokně **Přidat role do projektu** v poli **Role** vyberte **Člen týmu**. V poli **Počet prostředků** zadejte hodnotu **5**.
11. Vyberte **Vytvořit**.
12. Na stránce **Projekty** vyberte **Splnit prostředek**.

## <a name="monitor-project-teams"></a>Monitorování projektových týmů
1. Na stránce **Všechny projekty** vyberte odkaz **ID projektu** pro projekt **Upgrade XYZ fáze 2**.
2. Na pevné záložce **Projektový tým a plánování** ověřte správnost uvedených prostředků.
