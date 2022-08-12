---
title: Odebrání instance
description: Tento článek popisuje proces odebrání zkušební jednotky nebo výrobního prostředí pro aplikaci Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0ce676c93e133cc04ad9c49417ed2ca0d6791e93
ms.sourcegitcommit: 1401d66b6b64c590ca1f8f339d622e922920cf15
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/20/2022
ms.locfileid: "9178465"
---
# <a name="remove-an-instance"></a>Odebrání instance

_**Platí pro:** Human Resources na samostatné infrastruktuře_ 

> [!NOTE]
> Od července 2022 nebude možné v samostatné infrastruktuře Human Resources zřizovat nová prostředí Human Resources a projekty Microsoft Dynamics Lifecycle Services (LCS) na něm nelze vytvářet. Zákazníci mohou nasadit prostředí Human Resources na finanční a provozní infrastrukturu. Více informací viz [Zřízení Human Resources ve finanční a provozní infrastruktuře](/hr-admin-setup-provision-fo.md).

> [!IMPORTANT]
> Infrastruktura finančních a provozních aplikací podporuje odstranění prostředí. Další informace o tom, jak odstranit prostředí, viz [Odstranění prostředí](../fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure.md#delete-an-environment).

Tento článek vám vysvětlí proces odebrání zkušební jednotky nebo výrobního prostředí pro aplikaci Microsoft Dynamics 365 Human Resources.

## <a name="remove-a-test-drive-environment"></a>Odebrání testovacího prostředí

Testovací jednotky aplikace Human Resources jsou zřizovány s 60denním vypršením platnosti. Vlastníci prostředí testovací jednotky však mají možnost ukončit své zkušební verze dříve podle následujícího postupu. 

1. Přejděte do [Centra pro správu Power Apps](https://admin.businessplatform.microsoft.com/).
2. Vyberte **Prostředí**.
3. Vyberte testovací prostředí, které má podobný vzorec pojmenování jako tento: TestDrive - alias@domain
4. Vyberte **Odstranit** a potvrďte rozhodnutí. 

Existující testovací prostředí bude odstraněno. Po odebrání se můžete přihlásit k novému testovacímu prostředí. 

## <a name="remove-a-production-environment"></a>Odebrání produkčního prostředí

Tento článek předpokládá, že jste si zakoupili aplikaci Human Resources prostřednictvím poskytovatele cloudového řešení (CSP) nebo smlouvy o podnikové architektuře (EA). 

Vzhledem k tomu, že jedno prostředí aplikace Human Resources je obsaženo v jednom prostředí Power Apps, při odstraňování prostředí existují dvě možnosti ke zvážení. 
- **Odstranění celého prostředí Power Apps.** Tato volba je upřednostňována při vytvoření prostředí Power Apps výslovně za účelem zřízení aplikace Human Resources, při začátku implementace, nebo když nemáte žádné ustavené integrace.  
- **Odstranění pouze Human Resources.** Tato možnost je vhodná, pokud máte zřízené prostředí Power Apps naplněné mnoha daty, která jsou využita v Microsoft Power Apps a Power Automate.


> [!Important]
> Před odstraněním prostředí Power Apps ověřte, že se již nepoužívá pro datové integrace mimo aplikaci Human Resources. Povšimněte si též, že výchozí prostředí Power Apps nelze odstranit. 

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
4. Přihlaste se do LCS pomocí účtu, který jste použili pro přihlášení k odběru aplikace Human Resources. 
5. Vyberte projekt Human Resources obsahující prostředí. 
6. Ve svém LCS projektu vyberte dlaždici **Správa aplikace Human Resources**. 
7. Vyberte instanci, kterou chcete odebrat. Ta by měla být označena stavem nasazení **Odstraněný**.
8. Vyberte **Odebrat instanci** a potvrďte vaše rozhodnutí. 

## <a name="recover-a-soft-deleted-environment"></a>Obnovte prostředí s logickým odstraněním

Pokud odstraníte prostředí Power Apps, ke kterému je vaše prostředí Human Resources připojeno, bude stav prostředí Human Resources ve službě LCS **Logicky odstraněno**. V tomto případě se uživatelé nemohou připojit k Human Resources.

Postup obnovení prostředí:

1. Postupujte podle pokynů v [Obnovení prostředí Power Apps](/power-platform/admin/recover-environment).

2. Chcete-li obnovit prostředí Human Resources, kontaktujte podporu. Pro další informace si přečtěte [Získání podpory](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

> [!Warning]
> Prostředí Power Apps jsou uložena pouze po dobu sedmi dnů po odstranění. Prostředí musíte obnovit do sedmi dnů.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
