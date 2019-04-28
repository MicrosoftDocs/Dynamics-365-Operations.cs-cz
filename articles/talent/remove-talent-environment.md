---
title: Odstranění prostředí Talent
description: Toto téma vás povede procesem odebrání zkušební jednotky nebo výrobního prostředí pro aplikaci Dynamics 365 for Talent.
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: 904c8eb1254a65e1627c33f14488a1a8e12f7c2b
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/19/2019
ms.locfileid: "858875"
---
# <a name="remove-talent-environments"></a>Odstranění prostředí Talent

[!include [banner](includes/banner.md)]

Toto téma vás povede procesem odebrání zkušební jednotky nebo výrobního prostředí pro aplikaci Dynamics 365 for Talent.

## <a name="removing-a-test-drive-environment"></a>Odstranění testovacího prostředí

Testovací jednotky Talent jsou zřizovány s 60denním vypršením platnosti. Vlastníci prostředí testovací jednotky však mají možnost ukončit své zkušební verze dříve podle následujícího postupu. 

1. Přejděte na [Centrum správy PowerApps](https://admin.businessplatform.microsoft.com/).
2. Vyberte **Prostředí**.
3. Vyberte testovací prostředí, které má podobný vzorec pojmenování jako tento: TestDrive - alias@domain
4. Vyberte **Odstranit** a potvrďte rozhodnutí. 

Existující testovací prostředí bude odstraněno. Po odebrání se můžete přihlásit k novému testovacímu prostředí. 

## <a name="removing-a-production-environment"></a>Odstranění produkčního prostředí

Toto téma předpokládá, že jste si zakoupili aplikaci Talent prostřednictvím poskytovatele cloudového řešení (CSP) nebo smlouvy o podnikové architektuře (EA). 

Vzhledem k tomu, že jedno prostředí Talent je obsaženo v jednom prostředí PowerApps, existují dvě možnosti ke zvážení. První možnost zahrnuje odebrání celého prostředí PowerApps; druhá možnost vyžaduje odebrání pouze aplikace Talent. První volba je upřednostňována při vytvoření prostředí PowerApps výslovně za účelem zřízení aplikace Talent a při začátku implementace, nebo když nemáte žádné ustavené integrace. Druhá možnost je vhodná, pokud máte zřízené prostředí PowerApps naplněné mnoha daty, která jsou využita v PowerApps a tocích.

> [!Important]
> Před odstraněním prostředí PowerApps ověřte, že se již nepoužívá pro bohaté datové integrace mimo aplikaci Talent. Povšimněte si též, že výchozí prostředí PowerApps nelze odstranit. 

Chcete-li odebrat celé prostředí PowerApps, včetně prostředí Talent a přidružených aplikací a toků:

1. Přejděte na [Centrum správy PowerApps](https://admin.businessplatform.microsoft.com/).
2. Vyberte **Prostředí**.
3. Vyberte prostředí, které má být odstraněno.
4. Vyberte **Odstranit** a potvrďte rozhodnutí. 
5. Počkejte, dokud není dokončeno odstranění.
6. Přihlaste se do [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) pomocí účtu, který jste použili pro přihlášení se k odběru aplikace Talent. 
7. Vyberte projekt Talent obsahující prostředí. 
8. Ve svém LCS projektu vyberte dlaždici **Správa aplikace Talent**. 
9. Vyberte instanci, kterou chcete odebrat. 
10. Vyberte **Odebrat instanci** a potvrďte vaše rozhodnutí.  

Chcete-li odebrat prostředí Talent z existujícího prostředí PowerApps, proveďte následující kroky. Všimněte si, že nutnost zahrnout podporu a kontaktovat tým Talent DevOps je dočasná, dokud tato funkce nebude povolena přímo v LCS.

1. Požádejte podporu o zahájení požadavku na odebrání.
2. Tým podpory iniciuje požadavek na odebrání s týmem Talent DevOps. 
3. Pokračujte po zobrazení informace, že bylo prostředí odebráno.
4.  Přihlaste se do LCS pomocí účtu, který jste použili pro přihlášení se k odběru aplikace Talent. 
5. Vyberte projekt Talent obsahující prostředí. 
6. Ve svém LCS projektu vyberte dlaždici **Správa aplikace Talent**. 
7. Vyberte instanci, kterou chcete odebrat. Ta by měla být označena stavem nasazení **Neúspěšný**.
8. Vyberte **Odebrat instanci** a potvrďte vaše rozhodnutí. 

