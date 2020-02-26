---
title: Odebrání instance
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5c5f875ad9361c31af4fbe863488b881cdd97a6e
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008307"
---
# <a name="remove-an-instance"></a>Odebrání instance

Tento článek vás provede procesem odebrání zkušební jednotky nebo výrobního prostředí pro aplikaci Microsoft Dynamics 365 Human Resources.

## <a name="remove-a-test-drive-environment"></a>Odebrání testovacího prostředí

Testovací jednotky aplikace Human Resources jsou zřizovány s 60denním vypršením platnosti. Vlastníci prostředí testovací jednotky však mají možnost ukončit své zkušební verze dříve podle následujícího postupu. 

1. Přejděte do [Centra pro správu Power Apps](https://admin.businessplatform.microsoft.com/).
2. Vyberte **Prostředí**.
3. Vyberte testovací prostředí, které má podobný vzorec pojmenování jako tento: TestDrive - alias@domain
4. Vyberte **Odstranit** a potvrďte rozhodnutí. 

Existující testovací prostředí bude odstraněno. Po odebrání se můžete přihlásit k novému testovacímu prostředí. 

## <a name="remove-a-production-environment"></a>Odebrání produkčního prostředí

Tento článek předpokládá, že jste si zakoupili aplikaci Human Resources prostřednictvím poskytovatele cloudového řešení (CSP) nebo smlouvy o podnikové architektuře (EA). 

Vzhledem k tomu, že jedno prostředí aplikace Human Resources je obsaženo v jednom prostředí Power Apps, existují dvě možnosti ke zvážení. První možnost zahrnuje odebrání celého prostředí Power Apps; druhá možnost vyžaduje odebrání pouze aplikace Human Resources. První volba je upřednostňována při vytvoření prostředí Power Apps výslovně za účelem zřízení aplikace Human Resources a při začátku implementace, nebo když nemáte žádné ustavené integrace. Druhá možnost je vhodná, pokud máte zřízené prostředí Power Apps naplněné mnoha daty, která jsou využita v Power Apps a Power Automate.

> [!Important]
> Před odstraněním prostředí Power Apps ověřte, že se již nepoužívá pro bohaté datové integrace mimo aplikaci Human Resources. Povšimněte si též, že výchozí prostředí Power Apps nelze odstranit. 

Chcete-li odebrat celé prostředí Power Apps, včetně prostředí Human Resources a přidružených aplikací a toků:

1. Přejděte do [Centra pro správu Power Apps](https://admin.businessplatform.microsoft.com/).
2. Vyberte **Prostředí**.
3. Vyberte prostředí, které má být odstraněno.
4. Vyberte **Odstranit** a potvrďte rozhodnutí. 
5. Počkejte, dokud není dokončeno odstranění.
6. Přihlaste se do [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) pomocí účtu, který jste použili pro přihlášení se k odběru aplikace Human Resources. 
7. Vyberte projekt Human Resources obsahující prostředí. 
8. Ve svém LCS projektu vyberte dlaždici **Správa aplikace Human Resources**. 
9. Vyberte instanci, kterou chcete odebrat. 
10. Vyberte **Odebrat instanci** a potvrďte vaše rozhodnutí.  

Chcete-li odebrat prostředí Human Resources z existujícího prostředí Power Apps, proveďte následující kroky. Všimněte si, že nutnost zahrnout podporu a kontaktovat tým Human Resources DevOps je dočasná, dokud tato funkce nebude povolena přímo v LCS.

1. Požádejte podporu o zahájení požadavku na odebrání.
2. Tým podpory iniciuje požadavek na odebrání s týmem Human Resources DevOps. 
3. Pokračujte po zobrazení informace, že bylo prostředí odebráno.
4.  Přihlaste se do LCS pomocí účtu, který jste použili pro přihlášení k odběru aplikace Human Resources. 
5. Vyberte projekt Human Resources obsahující prostředí. 
6. Ve svém LCS projektu vyberte dlaždici **Správa aplikace Human Resources**. 
7. Vyberte instanci, kterou chcete odebrat. Ta by měla být označena stavem nasazení **Neúspěšný**.
8. Vyberte **Odebrat instanci** a potvrďte vaše rozhodnutí. 
