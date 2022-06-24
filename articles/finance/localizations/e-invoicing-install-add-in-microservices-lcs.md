---
title: Instalace doplňku pro mikroslužby ve službě Lifecycle Services
description: Tento článek vysvětluje, jak nainstalovat doplněk Elektronická fakturace ve službě Microsoft Dynamics Lifecycle Services (LCS).
author: dkalyuzh
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 26f92262eff07ded3e894ee5513dd8dbaa6f94a4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849798"
---
# <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>Nainstalujte doplněk pro mikroslužby ve službě Lifecycle Services

[!include [banner](../includes/banner.md)]

Ověřování ve službě Elektronická fakturace vyžaduje, abyste si zaregistrovali své prostředí Microsoft Dynamics 365 Finance nebo Dynamics 365 Supply Chain Management v platformě služeb, a to instalací doplňku pro vaše prostředí ve službě Microsoft Dynamics Lifecycle Services (LCS).

Při registraci prostředí postupujte takto.

1. Přihlaste se k účtu LCS.
2. Na řídicím panelu projektu vyberte projekt LCS.
2. V projektu vyberte na řídicím panelu **prostředí** své prostředí pro nasazení. Prostředí, které vyberete, musí být spuštěné.
3. Na kartě **Integrace Power Platform** v sekci **Doplňky prostředí** vyberte **Instalovat nový doplněk**.
4. Vyberte **Nastavení elektronické fakturace**.
5. V poli **ID aplikace AAD** zadejte **091c98b0-a1c9-4b02-b62c-7753395ccabe**. Tato hodnota je pevná hodnota. Ujistěte se, že zadáváte pouze globálně jedinečný identifikátor (GUID). Nevkládejte žádné další symboly, jako jsou mezery, čárky, tečky nebo uvozovky.
6. V poli **ID klienta AAD** zadejte ID tenanta účtu předplatného Azure. Klient Azure Active Directory (Azure AD), kterého zadáte, by měl být stejný jako ten, který se používá pro služby Regulatory Configuration Service (RCS).
7. Zkontrolujte smluvní podmínky a poté zaškrtněte políčko.
8. Vyberte **Instalovat**. Po několika minutách by se stav měl změnit z **Probíhá instalace** na **Nainstalováno**. Možná bude nutné pro zobrazení této změny aktualizovat stránku.

Elektronická fakturace je nyní připravena k použití.

> [!NOTE]
> Společnosti mají obvykle několik prostředí Finance nebo Supply Chain Management. Tato prostředí zahrnují produkční prostředí, prostředí akceptačního testování uživatele (UAT) a vývojová prostředí (sandbox). Předchozí proceduru musíte potvrdit pro všechna prostředí, která chcete připojit k funkci Elektronické fakturace.
