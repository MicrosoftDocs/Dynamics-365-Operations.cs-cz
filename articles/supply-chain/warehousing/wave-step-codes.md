---
title: Kódy kroku vlny
description: V tomto tématu je uveden přehled kódů kroků vlny a jejich použití.
author: josaw1
manager: tfehr
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 251e9982451c888424589e0f0d6fce48aab42df1
ms.sourcegitcommit: 68092ed283bfbb7b6f611cce1b62c791f9b6a208
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/30/2020
ms.locfileid: "3323570"
---
# <a name="wave-step-codes"></a>Kódy kroku vlny

[!include [banner](../includes/banner.md)]

Kódy kroků vlny jsou kódy, které mohou uživatelé nastavit a použít k propojení určitých instancí metod vlny s odpovídající šablonou. Tyto šablony zahrnují šablony pro doplnění, vytváření kontejnerů, tisk štítků, sestavení a třídění.

Nejsou-li kódy kroků vlny použity, uživatelé musí zadat volný text, který bude odkazovat na určitou šablonu z instance metody vlny. Volný text je náchylný k chybám, protože uživatelé se musí ujistit, že text kroku vlny, který přidávají pro specifickou metodu vlny v šabloně vlny, přesně odpovídá textu kroku vlny v cílové šabloně.

Kódy kroků vlny pro určitý typ kroku vlny jsou nastaveny na samostatné stránce. Pro každou instanci metody kroku vlny v šabloně vlny, která vyžaduje kód kroku vlny, musí být v rozevíracím seznamu vybrán kód kroku vlny. Výběr v rozevíracím seznamu nahrazuje zadávání volného textu a pomáhá snižovat riziko a dopad lidských chyb. Kódy nastavení se používají k propojení metody kroku vlny v šabloně vlny s cílovou šablonou pro metodu.

> [!NOTE]
> Použití funkce kódů kroku vlny je nepovinné. Je povolena celá organizace pro všechny právnické osoby.

## <a name="setup-demo"></a>Nastavení ukázky 

Pro tuto ukázku musíte mít nainstalována ukázková data a musíte použít ukázkovou společnosti **USMF**.

### <a name="enable-wave-step-codes"></a>Povolit kódy kroku vlny

Pomocí následujících kroků zapněte funkci kódů kroků vlny.

1. Přejděte na **Správu funkcí**.
2. Výběrem této možnosti povolíte funkci nazvanou **Kód kroku vlny pro celou organizaci**.

Všechny existující volné texty ve všech právnických osobách jsou upgradovány na novou strukturu. Po dokončení upgradu pro všechny právnické osoby je tato funkce povolena. Pokud funkci nelze povolit pro jednu nebo více právnických osob, nebude tato funkce povolena pro žádné právnické osoby.

Během upgradu jsou během inovace dat provedeny ověření. Pokud se inovace nezdaří, zobrazí se chybová zpráva. Upgrade se nemusí zdařit kvůli následujícím konfliktům:

- Existují duplicitní texty volného kroku vlny.
- Existují přizpůsobení.
- Volný text v kroku vlny, který je přidružen k instanci metody kroku vlny, neodpovídá očekávanému typu šablony.

Po vyřešení konfliktů, které byly zjištěny během ověření, můžete znovu zkusit povolit funkci.

Po povolení funkce bude k dispozici stránka **kódy kroků vlny** (**Řízení skladu \> Nastavení \> Vlny \> Kódy nastavení vlny**). Na této stránce jsou uvedeny kódy kroků vlny, které byly upgradovány při zapnutí funkce kódy kroků vlny pro celou organizaci.

### <a name="create-new-wave-step-codes"></a>Vytvořit nové kódy kroků vlny

Stránku **kódy kroků vlny** můžete použít k vytváření a odstraňování kódů kroků vlny.

Každý nový kód kroku vlny a jeho přidružené ID musí být jedinečné napříč všemi typy kroků vlny a musí být definovány pro určitý typ kroku vlny.

### <a name="apply-wave-step-codes"></a>Použití kódů kroků vlny

Po definování příslušných kódů kroků vlny je lze použít na metody procesu vlny.

Chcete-li použít kódy kroků vlny, přejděte na příslušnou cílovou šablonu. Zde jsou cílové šablony, pro které jsou označeny kódy kroků vlny na:

- **Šablony doplnění:** Řízení skladu \> Nastavení \> Doplnění \> Šablony doplnění
- **Načíst šablony sestavení:** Řízení skladu \> Nastavení \> Načíst \> Načíst šablony sestavení
- **Seřadit šablony:** Řízení skladu \> Nastavení \> Balení \> Odchozí šablony řazení
- **Šablony vytváření kontejnerů:** Řízení skladu \> Nastavení \> Kontejnery \> Šablony sestavení kontejneru
- **Štítky pro tisk štítků**: Řízení skladu \> Nastavení \> Směrování dokumentu \> Šablony štítku vlny

Šablony v tomto seznamu jsou použity, pokud jsou odkazovány z metody procesu vlny vybrané v šabloně vlny. Když kód kroku vlny u metody procesu vlny v šabloně vlny odpovídá kódu kroku vlny v jednom z typů šablon, použije se šablona.

### <a name="sample-scenario"></a>Ukázkový scénář

Následující postup vám pomůže zaručit, že vytvořená šablona doplnění bude použita pro šablonu vlny.

1. Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Kódy kroku vlny** a vytvořte kód kroku vlny pro typ **doplnění**.
2. Přejděte na **Řízení skladu \> Nastavení \> Doplnění \> Šablony doplnění** a vytvořte šablonu doplnění.
3. V šabloně doplnění vyberte kód kroku vlny, který jste vytvořili pro typ **doplnění**.
4. Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny** a vyberte šablonu vlny, kterou chcete použít.
5. V šabloně na pevné záložce **Metody** vyberte metodu **Doplnění**.
6. V poli **Kód kroku vlny** vyberte kód kroku vlny, který jste vybrali v šabloně doplnění.

Tyto kroky provedete pro každou právnickou osobu.
