---
title: "Nastavení pro správu v aplikaci Attract"
description: "Toto téma vysvětluje postup povolení fungování funkce pro organizace uživatele v aplikaci Attract."
author: 
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 52b48d5daab985c43d59f29ad7b80dda99a7fcef
ms.contentlocale: cs-cz
ms.lasthandoff: 10/22/2018

---

# <a name="admin-settings-in-attract"></a>Nastavení pro správu v aplikaci Attract
[!include[banner](../includes/banner.md)]

Centrum pro správu v aplikaci Microsoft Dynamics 365 for Talent: Aplikace Attract obsahuje nastavení konfigurace, možnosti integrace a možnosti nastavení aplikace Attract.

## <a name="company-information"></a>Informace o společnosti

Zadejte zobrazovaný název společnosti a přidejte logo společnosti. Zobrazovaný název a logo lze pak použít při zveřejnění pracovních nabídek a během nástupu do zaměstnání.

## <a name="linkedin-integration"></a>Integrace se službou LinkedIn

Nastavte integraci se systémem LinkedIn Recruiter System Connect (RSC). Po připojení ke službě LinkedIn pomocí vašich přihlašovacích údajů na LinkedIn můžete synchronizovat profil uchazeče na webu LinkedIn, aplikace, zpětnou vazbu k pohovoru a poznámky náborového týmu. Je požadována úplná licence náboráře LinkedIn. Další informace o RSC získáte v tématu [Recruiter System Connect (RSC) – nejčastější dotazy](https://www.linkedin.com/help/recruiter/answer/90483).

## <a name="user-permissions"></a>Oprávnění uživatele

Proveďte přiřazení rolí uživatelům ve vaší organizaci. K dispozici jsou následující role: **Správce**, **náborář**, **Manažer náboru** a **jen pro čtení**. Další informace o uživatelských oprávněních naleznete v tématu [Zabezpečení a správa rolí v aplikaci Attract](./security-attract.md).

## <a name="feature-management"></a>Správa funkcí

Při přidávání nových funkcí se může zobrazit jejich vydání ve veřejném náhledu. Funkce veřejného náhledu nesplňují všechny požadavky na služby. Jejich přijetím souhlasíte, že budete sdílet své údaje s externími systémy. Můžete zjistit, že vaše organizace nevyžaduje všechny nové funkce, které jsou vydávány. Funkce veřejného náhledu můžete zapínat a vypínat podle potřeb vaší organizace.

## <a name="template-management"></a>Správa šablony

Šablona procesu obsahuje všechny aktivity, které mají být zahrnuty jako součást náborového procesu na danou pracovní pozici. Vaše organizace může povolit vytváření šablon procesu náboru všem členům týmu nebo jen správcům. Pokud chcete členům týmu povolit vytváření vlastních šablon procesu náboru, zapněte funkci Správa šablon. Další informace o šablonách procesu naleznete v tématu [Šablony procesu v aplikaci Attract](./process-templates-attract.md).

## <a name="email-template-settings"></a>Nastavení šablony e-mailu

Organizace mohou vytvořit šablony e-mailu pro různé scénáře. Můžete vybrat obrázek v záhlaví, který má být zahrnut do šablon e-mailu. Vybrané záhlaví se pak zobrazí ve všech e-mailových šablonách. V zápatí šablony můžete přidat odkaz na prohlášení o zásadách ochrany osobních údajů organizace a podmínky použití při komunikaci. Další informace naleznete v tématu [Šablony e-mailu v aplikaci Attract](./email-templates.md).

## <a name="offer-process"></a>Proces nabídky

Můžete nakonfigurovat schvalovací proces pro nabídky pracovního místa. Můžete například určit, zda nabídka musí být schválena před odesláním uchazeči. Můžete také požadovat, aby schvalující u rozhodnutí o nabídce uvedli komentář.

K dispozici jsou dva pracovní postupy schválení: **paralelní** a **sekvenční**.

- **Paralelní** – schválení jsou zaslána všem schvalovatelům současně.
- **Sekvenčí** – Schválení jsou zasílána schvalovatelům v konkrétním pořadí.

Můžete také konfigurovat možnosti, které souvisejí se zkušenostmi uchazeče. Například jedna z možností umožňuje určit, zda mohou uchazeči nabídku zamítnout bez další diskuse. Pokud nastavíte možnost **Povolit uchazečům odmítnutí nabídky bez další diskuse** na **Ne**, budou mít uchazeči k dispozici tlačítko **Odmítnout nabídku**. Pokud tuto možnost nastavíte na **Ano**, uchazeči můžou nabídku odmítnout výběrem důvodu a potom kliknout na **Odmítnout nabídku**.

Můžete také nastavit a vynutit datum vypršení platnosti nabídek. Nastavíte-li možnost **Vyžadovat datum vypršení platnosti pro všechny nabídky** na **Ano**, nabídky přestanou platil po zadaném počtu dní nebo hodin.

Další informace o správě nabídky získáte v části [Nastavení správy nabídky](./offer-setup.md).
