---
title: Kódy kroku vlny
description: V tomto tématu je uveden přehled kódů kroků vlny a jejich použití.
author: josaw1
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f89c6098db9e2e3a9aa4ee3666e4b9ae608f054
ms.sourcegitcommit: d8f1135cdbc2deca70bc4b2805a0519253c9a31f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/06/2019
ms.locfileid: "1992350"
---
# <a name="wave-step-codes"></a>Kódy kroku vlny

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

## <a name="about-wave-step-codes"></a>Informace o kódech kroků vlny

Kódy kroků vlny jsou kódy, které mohou uživatelé nastavit a použít k propojení určitých instancí metod vlny s odpovídající šablonou. Tyto šablony zahrnují šablony pro doplnění, vytváření kontejnerů, tisk štítků, sestavení a třídění.

Nejsou-li kódy kroků vlny použity, uživatelé musí zadat volný text, který bude odkazovat na určitou šablonu z instance metody vlny. Volný text je náchylný k chybám, protože uživatelé se musí ujistit, že text kroku vlny, který přidávají pro specifickou metodu vlny v šabloně vlny, přesně odpovídá textu kroku vlny v cílové šabloně.

Kódy kroků vlny pro určitý typ kroku vlny jsou nastaveny na samostatné stránce. Pro každou instanci metody kroku vlny v šabloně vlny, která vyžaduje kód kroku vlny, musí být v rozevíracím seznamu vybrán kód kroku vlny. Výběr v rozevíracím seznamu nahrazuje zadávání volného textu a pomáhá snižovat riziko a dopad lidských chyb. Kódy nastavení se používají k propojení metody kroku vlny v šabloně vlny s cílovou šablonou pro metodu.

> [!NOTE]
> Použití funkce kódů kroků vlny je volitelné a přijetí je pro právnickou osobu. Pokud tedy určitá právnická osoba používá funkci, budou všechny stávající kódy kroků vlny v dané právnické osobě upgradovány na novou strukturu.

## <a name="setup-demo"></a>Nastavení ukázky 

Pro tuto ukázku musíte mít nainstalována ukázková data a musíte použít ukázkovou společnosti **USMF**.

### <a name="enable-wave-step-codes"></a>Povolit kódy kroku vlny

Pomocí následujících kroků zapněte funkci kódů kroků vlny.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Parametry řízení skladu**.
2. Na kartě **Obecné** na pevné záložce **Zpracování vlny** nastavte možnost **Povolit kódy vlny** na **Ano**.

Všechny existující volné texty kódu vlny jsou upgradovány na novou strukturu. Po dokončení tohoto upgradu pro právnickou osobu již není na možnost **Povolit kódy kroku vlny** na stránce **Parametry řízení skladu** k dispozici.

Ověření jsou prováděna během upgradu a pokud se upgrade nezdaří, zobrazí se chybová zpráva. Upgrade se nemusí zdařit kvůli následujícím konfliktům:

- Existují duplicitní texty volného kroku vlny.
- Existují přizpůsobení.
- Volný text v kroku vlny, který je přidružen k instanci metody kroku vlny, neodpovídá očekávanému typu šablony.

Po vyřešení konfliktů, které byly zjištěny během ověření, můžete znovu spustit proces upgradu.

Po úspěšném dokončení upgradu bude k dispozici stránka **kódy kroků vlny** (**Řízení skladu \> Nastavení \> Vlny \> Kódy nastavení vlny**). Na této stránce jsou uvedeny kódy kroků vlny, které byly upgradovány při zapnutí funkce kódy kroků vlny.

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
