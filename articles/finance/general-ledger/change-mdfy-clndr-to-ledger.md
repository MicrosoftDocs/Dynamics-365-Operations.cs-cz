---
title: Změna nebo opětovné přiřazení kalendáře hlavní knihy
description: Toto téma vysvětluje, jak změnit kalendář, který je aktuálně přiřazen k hlavní knize, a jak přiřadit k hlavní knize nový kalendář.
author: kweekley
ms.date: 05/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-07
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 25777a5b807921acc13338116627e9356fe62a20
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711624"
---
# <a name="change-or-reassign-a-ledger-calendar"></a>Změna nebo opětovné přiřazení kalendáře hlavní knihy

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak změnit kalendář, který je aktuálně přiřazen k hlavní knize, a jak přiřadit k hlavní knize nový kalendář.

## <a name="issue"></a>Problém

Společnosti někdy musí buď změnit existující kalendář, který je přiřazen k hlavní knize, nebo přiřadit nový kalendář.

## <a name="resolution"></a>Řešení

Jsou dva scénáře změny nebo opětovného přiřazení kalendáře hlavní knihy. První scénář zahrnuje změnu existujícího kalendáře, který je již k hlavní knize přiřazen. Druhý scénář zahrnuje vytvoření nového kalendáře a jeho přiřazení k hlavní knize. Obě změny lze provést kdykoli, a to i po zaúčtování transakcí do hlavní knihy.

### <a name="change-an-existing-fiscal-calendar"></a>Změna existujícího fiskálního kalendáře

Chcete-li změnit existující kalendář, který je přiřazen k hlavní knize, přejděte k nabídce **Hlavní kniha \> Nastavení hlavní knihy \> Hlavní kniha** a výběrem odkazu na fiskální kalendář otevřete stránku **Kalendáře hlavní knihy**.

Na změny, které lze v kalendáři provést, se vztahují limity. Můžete například změnit počáteční a koncové datum *období* v roce, ale nemůžete změnit počáteční a koncové datum *roku* v kalendáři.

Chcete-li změnit období v roce, vyberte příslušný kalendář a rok. Nejprve použijte tlačítko **Odstranit období**, abyste odstranili některá nebo všechna existující provozní období. Odstranit lze všechna provozní období kromě prvního. Poté použijte tlačítko **Rozdělit období**, abyste zadáním příslušného počátečního data dalšího období rozdělili zbývající jedno nebo více období na nová období.

Jakmile změníte období v kalendáři, musíte spustit proces **Přepočítat období hlavní knihy** v každé právnické osobě (společnosti), ke které je kalendář přiřazen. Přestože žádná varovná zpráva nepřipomíná, abyste tento krok provedli, proces přepočtu je nutný k aktualizaci období, které je přiřazeno každé zaúčtované transakci v hlavní knize. Chcete-li spustit proces přepočtu, vyberte pro každou společnost možnost **Přepočítat období hlavní knihy** na stránce **Nastavení hlavní knihy**.

Pokud není proces přepočtu spuštěn, transakční zůstatky v předvaze nebo na finančních výkazech mohou být zahrnuty do období nesprávně. V takovém případě můžete zůstatky kdykoli opravit spuštěním procesu přepočtu.

### <a name="assign-a-new-fiscal-calendar"></a>Přiřazení nového fiskálního kalendáře

Chcete-li přiřadit nový fiskální kalendář, přejděte na **Hlavní kniha \> Nastavení hlavní knihy \> Hlavní kniha** a vyberte **Upravit**, aby stránka **Hlavní kniha** přešla do režimu úprav. Pak vyberte v poli **Fiskální kalendář** nový fiskální kalendář.

Po změně fiskálního kalendáře hlavní knihy musíte spustit volbu **Přepočítat období hlavní knihy**. Když k hlavní knize přiřadíte nový fiskální kalendář, zobrazí se zpráva, která vám pomůže tento krok dokončit. Přestože zpráva může znít, že je proces přepočtu volitelný, ve skutečnosti není. Je nutné aktualizovat období, které je přiřazeno ke každé zaúčtované transakci v hlavní knize. Chcete-li spustit proces přepočtu, vyberte možnost **Přepočítat období hlavní knihy** na stránce **Nastavení hlavní knihy**.

Pokud není proces přepočtu spuštěn, transakční zůstatky v předvaze nebo na finančních výkazech mohou být zahrnuty do období nesprávně. V takovém případě můžete zůstatky kdykoli opravit spuštěním procesu přepočtu.
