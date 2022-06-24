---
title: Dopad na rozšiřitelnost katalogů Commerce pro přizpůsobení B2B
description: Tento článek popisuje vliv rozšiřitelnosti na funkci Katalogy Commerce pro B2B v Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 04/28/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: f21d3375db69dd412325d00261bfc18e26d0c257
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849008"
---
# <a name="extensibility-impact-of-commerce-catalogs-for-b2b-customizations"></a>Dopad na rozšiřitelnost katalogů Commerce pro přizpůsobení B2B

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tento článek popisuje vliv rozšiřitelnosti na funkci **Katalogy Commerce pro B2B** v Microsoft Dynamics 365 Commerce.

Pokud máte zájem o rozšíření kontextu katalogu na vlastní scénáře, možná bude nutné aktualizovat vaše přizpůsobení. Tato aktualizace se řídí standardním procesem, který musí zákazníci dodržovat, protože jejich přizpůsobení nemusí po provedení upgradu automaticky podporovat nejnovější funkce. Pokud vaše přizpůsobení zahrnují nějaké nové funkce nebo opravy chyb v jejich prostředí, doporučujeme odpovídajícím způsobem aktualizovat kód přizpůsobení. Tato aktualizace se podobá změnám, které společnost Microsoft provádí v základním kódu.

Projděte si případy přizpůsobení, které následují, a určete, zda je nutné aktualizovat vaše přizpůsobení.

> [!NOTE]
> - Všechna merchandisingová aplikační programová rozhraní (API) by měla být kompatibilní s katalogem. Proto je důležité, abyste předávali parametr **CatalogID**.
> - Výchozí katalog (**CatalogID**=**0**) není platným katalogem pro přihlášené uživatele typu business-to-business (B2B). Proto selžou všechna volání rozhraní API, která předají "0" nebo používají výchozí hodnotu, protože uživatelé webu nemají přístup ke katalogu 0. Chcete-li získat správné prostředí, musí být volání rozhraní API zákazníka aktualizována tak, aby předávala ID katalogu, který byl vybrán v ovládacím prvku výběru katalogu. Pokud použijete výchozí hodnotu a uživatel přepne katalogy, web by měl zobrazit data z vybraného katalogu. Proto by přizpůsobená rozhraní API měla předávat vybraný katalog, aby odpovídala rozhraním API, která jsou spouštěna ze základního kódu Commerce.

Následující případy přizpůsobení vyžadují vývojové aktualizace:

- **Případ 1:** Zákazník přijde se svou vlastní [datovou akcí](e-commerce-extensibility/data-actions.md) která volá API související s produktem nebo datovou akci. Následující kroky aktualizace jsou povinné:

    1. Pokud datová akce používá přímé volání API, aktualizujte datovou akci tak, aby předávala ID katalogu, jak ukazuje následující příklad.

        ![Aktualizovaná akce dat, která předává ID katalogu.](./media/customization1_a.png)

    1. Pokud datová akce volá jinou datovou akci související s produktem v rámci přizpůsobení, je nutné kód aktualizovat, aby předal některé nové parametry, jako např. **requestContext**. Parametr **requestContext** se používá k načtení aktuálního ID katalogu, jak ukazuje následující příklad.

        ![Aktualizovaná akce dat, která předává nový parametr.](./media/customization1_b.png)

- **Případ 2:** Zákazník má [přepsanou datovou akci](e-commerce-extensibility/data-action-overrides.md). Následující krok aktualizace je povinný:

    - Aktualizujte datovou akci jako v případě 1.

- **Případ 3:** Zákazník má k dispozici rozšíření zobrazení, modul injektoru skriptu, popř. [klonovaný modul](e-commerce-extensibility/modules-overview.md#clone-a-module-library-module) zahrnující volání rozhraní API nebo datových akcí. Následující krok aktualizace je povinný:

    - Aktualizujte kód jako v případě 1, jak ukazuje následující příklad.

       ![Aktualizovaný kód, který předává nový parametr.](./media/customization3.png)

- **Případ 4:** Zákazník používá volání API **getById**. Následující krok aktualizace je povinný:

    - Přepněte místo toho na volání API **getByIds**, protože volání API **getById** má určitá omezení a nepodporuje povědomí o katalogu.

- **Případ 5:** Zákazník má datovou akci, která načítá informace pro více produktů, které se mohou nacházet v různých katalozích. Následující krok aktualizace je povinný:

    - Rozdělte volání API podle ID katalogu. Například pro rozhraní API košíku může košík obsahovat produkty z různých katalogů. Produktové řady by měly být seskupeny podle ID katalogu a měly by volat rozhraní API pro každý katalog samostatně, jak ukazuje následující příklad.

        ![Aktualizovaná akce dat, která seskupuje produktové řady podle ID katalogu.](./media/customization5.png)

## <a name="additional-resources"></a>Další prostředky

[Vytváření obchodních katalogů pro B2B weby](catalogs-b2b-sites.md)

[Nejčastější dotazy k obchodním katalogům pro B2B](catalogs-b2b-sites-FAQ.md)
