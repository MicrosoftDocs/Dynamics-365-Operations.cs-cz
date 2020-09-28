---
title: Vytvořit nový projekt
description: Tohle téma obsahuje informace, jak vytvořit nový projekt.
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
ms.openlocfilehash: c8c52b8c1c86ea2f6e03cf439ba5930f1006ab4f
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760493"
---
# <a name="create-a-new-project"></a>Vytvořit nový projekt

[!include [banner](../includes/banner.md)]

Pomocí následujících kroků vytvoříte nový projekt.

1. Na stránce **Správa projektu** vyberte **Nový projekt** a zadejte následující hodnoty:

    - **Typ projektu:** Čas a materiál
    - **Název projektu:** Upgrade XYZ fáze 2
    - **Skupina projektu:** TM\_WIP
    - **ID projektové smlouvy:** 00000002

2. Zvolte **Vytvořit projekt**.

## <a name="assign-a-resource-to-a-project"></a>Přiřazení prostředku k projektu

1. Na stránce **Pracovníci** v seznamu **Pracovníci** vyberte záznam o zaměstnanci, pro kterého jste dříve nastavili kompetence, a otevřete záznam pracovníka.
2. V podokně akcí na kartě **Projekt** ve skupině **Nastavení** zvolte **Přiřadit projekty**.
3. Na stránce **Přiřazení projektů ověření prostředku** na kartě **Projekty** v poli **Přidat projekt do vybraných projektů** pole filtrujte na projektu **Upgrade XYZ fáze 2**.
4. V podokně **Zbývající projekty** vyberte projekt, zvolte tlačítko šipky a přidejte ho do podokna **Vybrané projekty**.

Podle potřeby můžete také přiřadit kategorie ke zdroji. Typ kategorie jsou buď **Náklady** nebo **Výnosy**. Typ kategorie je určen vaší organizací. Pokud neexistují žádné přiřazené kategorie pro zdroj, aplikace Finance vyhledává výchozí kategorii pro hodinové ceny pro náklady a výnosy.

## <a name="set-up-project-resource-and-role-characteristics"></a>Nastavení vlastností prostředků a role projektu

Manažer projektu může použít funkci přidělení prostředků k projektu pro vytvoření rolí potřebných pro daný projekt. Role lze použít, pokud potvrzené zdroje jsou během rezervace zdroje zatím neznámé. Role lze použít pro dočasné rezervování jako plánovaných zdrojů, abyste mohli pokračovat ve fázi plánování projektu.

[![Příklad role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scénář:** Společnost Contoso byla najata na dokončení projektu Čas a materiál, který má schválené stanovy projektu. Nižší manažer projektu stále dokončuje rozsah projektu. Manažer prostředků aktuálně identifikuje konkrétní zdroje, které budou rezervovány k práci na novém projektu. S ohledem na kritickou povahu projektu investor projektu požaduje, aby jedna z rolí byla vrchní vedoucí projektu. Správce zdrojů musí získat nový zdroj a rozhodne se, že určí roli v systému pro případ, že nižší manažer projektu bude potřebovat informace o zdroji během plánování projektu.

Následující pokyny popisují, jak může manažer prostředků nastavit roli Vrchní vedoucí projektu a přidružit k ní vlastnosti prostředků. Později slouží role k vyhledání dostupných zdrojů, které odpovídají požadovaným kompetencím prostředku.

1. Na stránce **Nastavení role** vyberte **Nová** a zadejte následující hodnoty:

    - **ID role:** vrchní manažer projektu
    - **Popis:** vrchní manažer projektu

2. Vyberte **Vytvořit**.
3. Vyberte roli **Vrchní manažer projektu** a zvolte **Konfigurace vlastností**.
4. V poli **Typ charakteristik** vyberte **Dovednost**.
5. V poli **Dostupné charakteristiky** zadejte hledanou dovednost.
6. V poli **Typ charakteristiky** vyberte **Certifikát**.
7. V poli **Dostupné charakteristiky** zadejte hledaný typ certifikátu.

## <a name="assign-a-project-resource-to-a-project"></a>Přiřazení prostředku projektu k projektu

1. Na stránce **Všechny projekty** vyberte projekt **Upgrade XYZ fáze 2**.
2. Na kartě **Projektový tým a plánování** zvolte **Přidat**.
3. V poli **Role** vyberte **Člen týmu**.
4. Zvolte **Rezervovat z kalendáře**.
5. Na stránce **Dostupnost prostředku** zvolte **Zobrazit nastavení**.
6. Na stránce **Upravit nastavení zobrazení** zadejte následující hodnoty:

    - **Formát pro zobrazení rozsahu dat:** den
    - **Zobrazit popisy dostupnosti:** ano
    - **Zobrazit zbývající kapacitu:** ano

7. V seznamu zdrojů vyberte prostředek.
8. Vyberte **Závazná rezervace** a **Plná kapacita**.

## <a name="assign-a-resource-to-a-default-role"></a>Přiřazení prostředku k jiné roli

Pokud chcete usnadnit práci manažerům projektu nebo zdrojů, můžete přejít hlouběji do podrobností zdrojů, které lze pro projekt rezervovat. Můžete přiřadit výchozí roli k existujícímu prostředku nebo nově získanému prostředku. Například když byl přijat Daniel, měl zkušenosti a schopnosti plnit roli obchodního analytika. Správce prostředků přiřadil tuto roli Danielovi jako výchozí. Proto správce prostředků přidal Daniela do fondu obchodních analytiků, kteří jsou k dispozici pro práci na projektech.

Během rezervování zdrojů mohou projektoví manažeři filtrovat zdroje v roli, které jsou k dispozici pro práci na projektech. Tyto údaje lze použít jako jednu z kritérií při provádění analýzy rozhodnutí s více kritérii během plnění prostředků. Mohou také přidat další charakteristiky prostředků do filtru a vyhledat zdroje, které mají určité dovednosti, vzdělání a zkušenosti s daným projektem.

**Situace:** začal schválený projekt a role Hlavní manažer projektu byla během fáze plánování projektu rezervována jako plánovaný zdroj. Manažer prostředků získá prostředek pro naplnění role Hlavní manažer projektu.

1. Na stránce **Seznam prostředků** vyberte **Daniel Goldschmidt**.
2. Na stránce **Role prostředku** vyberte **Nový** a zadejte následující hodnoty:

    - **Platnost:** Zadejte aktuální datum.
    - **Vypršení platnosti:** Zadejte **Nikdy**.
    - **Role:** Zadejte **Vrchní manažer projektu**.

3. Zvolte **Uložit** a pak zavřete stránku.
4. Na kartě **Kompetence** přidejte dovednost **ProjectMgmt** a certifikát **PMP**.
