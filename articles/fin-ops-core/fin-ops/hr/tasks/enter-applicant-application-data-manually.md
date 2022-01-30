---
title: Ruční zadávání dat o přihlášce a uchazeči
description: Tento postup popisuje, jak ručně spravovat informace o uchazečích a jejich přihláškách.
author: twheeloc
ms.date: 01/10/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmApplicant, LogisticsContactInfoGrid, HRMApplication,  DirPartyTable
audience: Application User
ms.reviewer: anbichse
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5305ded440dce0cf057e5fbe4df72635ce0e7b6b
ms.sourcegitcommit: 27475081f3d2d96cf655b6afdc97be9fb719c04d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/12/2022
ms.locfileid: "7964699"
---
# <a name="enter-applicant-and-application-data-manually"></a>Ruční zadávání dat o přihlášce a uchazeči

[!include [banner](../../includes/banner.md)]

Tento postup popisuje, jak ručně spravovat informace o uchazečích a jejich přihláškách. Můžete zadat a spravovat osobní údaje, data a časy pohovoru, odkazy, kompetence a požadavky na ubytování pro uchazeče. Také můžete aktualizovat stav uchazečových žádostí o zaměstnání a vytváření dopisů nebo e-mailových zpráv ke komunikaci s uchazeči. Při vytvoření záznamu žadatele se vytvoří osobní záznam tohoto uchazeče v globálním adresáři. K vytvoření této procedury jsou použita ukázková data společnosti **USMF**.

## <a name="create-a-new-applicant-record"></a>Vytvoření záznamu nového uchazeče

1. Přejděte na **Human Resources \> Nábor \> Uchazeči \> Uchazeči**.
2. Zvolte **Nové**.
3. Do pole **Křestní jméno** zadejte hodnotu.
4. Zadejte hodnotu do pole **Příjmení**.

    Pokud jsou k dispozici, můžete zadat další informace o žadateli. Tyto údaje mohou například zahrnovat nejvyšší vzdělání uchazeče, aktuální pracovní funkci nebo předchozího zaměstnavatele.

5. Rozbalte oddíl **Kontaktní informace**.
6. Vyberte **přidat**.
7. Do pole **Popis** zadejte **E-mail pro komunikaci**.
8. Vyberte volbu v poli **Typ**.
9. Zadejte hodnotu do pole **Kontaktní číslo/adresa**.

    Tento e-mailová adresa bude použita pro generování e-mailové komunikace s uchazečem.

10. Vyberte **přidat**.
11. V poli **Popis** zadejte hodnotu.
12. Zadejte hodnotu do pole **Kontaktní číslo/adresa**.

    Pomocí tohoto pole můžete podle potřeby zadat další osobní údaje o žadateli. Ty mohou například zahrnovat datum narození, údaje o etnickém původu, pohlaví nebo rodinný stav uchazeče.

13. V podokně akcí zvolte **Kompetence**.

    Můžete zadat profil kompetencí uchazeče, včetně jejich dovedností, profesionálních zkušeností, vzdělání, testů a certifikátů. Tyto informace slouží k mapování dovedností uchazeče k dovednostem spojeným s úlohami, které jsou definovány v datech společnosti.

## <a name="create-an-application-for-the-applicant"></a>Vytvoření přihlášky pro uchazeče

1. Vyberte **Přihlášky**.
2. Zvolte **Nové**.
3. V poli **Náborový projekt** vyberte šipku rozevíracího seznamu a otevřete vyhledávání.

    Výběrem náborového projektu zajistíte, že bude uchazeč přidružen ke konkrétní otevřené pozici zahrnuté v daném náborovém projektu.

4. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
5. Vyberte odkaz na vybraném řádku v seznamu.

    Ve výchozím nastavení je pozice a oddělení založeno na vybraném náborovém projektu.

6. Zvolte možnost **Uložit**.

    Po uložení aplikace k ní můžete připojit dokumenty. Tyto dokumenty mohou zahrnovat zkušenosti žadatele, ocenění a průvodní dopis.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
