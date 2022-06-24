---
title: Řídicí panel Správy využití
description: Tento článek vysvětluje, jak pomocí řídicího panelu Správa využití monitorovat používání služby elektronické fakturace a být v souladu s předpisy.
author: gionoder
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 3fad2acea373e96092208ce06edb31f1a862912d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875964"
---
# <a name="usage-management-dashboard"></a>Řídicí panel Správy využití

[!include [banner](../includes/banner.md)]

Řídicí panel **Správa využití** vám pomůže sledovat využití služby elektronické fakturace, a proto pomůže vaší organizaci zůstat v souladu s podmínkami měsíčního využití. Dodržování přepisů se určuje výpočtem objemu podání a jeho porovnáním se získaným objemem podání, aby se identifikovaly odchylky mezi získaným objemem a použitým objemem.

Řídicí panel obsahuje následující indikátory:

- Jeden indikátor nákladů, který můžete použít ke sledování spotřeby pro účely dodržování licenčních podmínek:

    - Využití za měsíc (export)

- Tři provozní indikátory, které můžete použít ke sledování využití služby elektronické fakturace pro účely správy:

    - Využití podle funkce
    - Využití podle prostředí
    - Využití za měsíc (import)

## <a name="measurement-scope"></a>Rozsah měření

- Měrná jednotka: 

    Řídicí panel **Správa využití** počítá odeslání obchodních dokumentů a importovaných elektronických faktur.

- Organizace: 

    Počítání je shrnuto podle ID klienta vaší organizace bez ohledu na počet instancí Microsoft Dynamics 365 Finance nebo Dynamics 365 Supply Chain Management, nebo počet právnických osob, kde je povolena služba elektronické fakturace.


## <a name="indicator-usage-per-month-export"></a>Ukazatel: Měsíční využití (export)

Tento indikátor poskytuje podrobnosti o elektronických fakturách, které vaše organizace vystavuje během definovaného období.

### <a name="scope"></a>Rozsah
- Počet obchodních dokumentů, které se odesílají z Finance a Supply Chain Management do služby elektronické fakturace, bez ohledu na počet řádků, které tyto obchodní dokumenty obsahují.
- Počet odeslaných obchodních dokumentů, které jsou úspěšně zpracovány službou elektronická fakturace. Dokument je považován za úspěšně zpracovaný, když je dokončen tok akcí definovaných v nastavení funkce.

> [!NOTE]
> Když je elektronická faktura odeslána do externí webové služby, počítání je nezávislé na výsledcích zpracování webové služby (přijato, odmítnuto nebo chyba ověření schématu). Pokud webová služba přijala a odpověděla na požadavek služby elektronické fakturace, je odeslání považováno za platné počítání.

- **Výjimka:** Obchodní dokumenty se nezapočítávají, pokud jsou znovu odeslány z Finance and Supply Chain Management do služby elektronické fakturace, například ve scénářích, kdy je pro změnu stavu elektronické faktury nutné opětovné odeslání stejného obchodního dokumentu. Například vystavení brazilské elektronické faktury (fiskálního dokumentu) se počítá jako platné, ale žádost o zrušení se nepočítá.


### <a name="calculation"></a>Výpočet

Výpočet zůstatku se počítá takto:

Zůstatek = zdarma + zakoupené - použité

Kde:

- Zdarma:
  
    Objem bchodních dokumentů, které může zákazník zdarma odeslat za měsíc. Zahrnuje balíček 100 obchodních dokumentů, které lze odeslat službě elektronické fakturace. Objem zdarma není kumulativní a zbývající zůstatek se nepřenesl do dalšího období.
  
- Zakoupené:
  
    Balíček 1 000 obchodních dokumentů, které lze odeslat službě elektronické fakturace. Tento balíček je nutné pro vaši organizaci získat každý měsíc. Zakoupený objem není kumulativní a zbývající zůstatek se nepřenesl do dalšího období.
  
- Použito: 

    Počet odeslání obchodních dokumentů do služby elektronické fakturace podle definovaných kritérií.
   
> [!IMPORTANT]
> Pokud vaše organizace plánuje překročit měsíční objem 100 bezplatných podání, zakupte si maximální objem, abyste zajistili, že budete i nadále v souladu s licenčními zásadami společnosti Microsoft pro službu elektronické fakturace.
>
> Aktuálně musí být zakoupený objem ručně zadán podle data pořízení jako více balíčků po 1 000 odesláních.

## <a name="indicator-usage-by-feature"></a>Indikátor: Využití podle funkce

Tento indikátor ukazuje využití funkcí elektronické fakturace pro vystavování elektronických faktur během definovaného období.

- Výpočet:
  
    Použité = Počet, kolikrát byla každá funkce elektronické fakturace použita při odesílání obchodních dokumentů službě elektronická fakturace.

## <a name="indicator-usage-by-environment"></a>Indikátor: Využití podle prostředí

Tento indikátor ukazuje využití prostředí služeb elektronické fakturace během definovaného období.

- Výpočet:
    
    Použité = Počet, kolikrát byla každé prostředí služby elektronické fakturace použita při odesílání obchodních dokumentů službě elektronická fakturace.

## <a name="indicator-usage-per-month-import"></a>Ukazatel: Měsíční využití (import)

Tento indikátor ukazuje objem importu elektronických faktur službou elektronická fakturace do Finance a Supply Chain Management za definované období.

- Rozsah:

    Elektronické faktury, které se importují do služby Finance a Supply Chain Management, bez ohledu na počet řádků, které tyto elektronické faktury obsahují.

- Výpočet:

    Přijato = Počet importovaných elektronických faktur do Finance a Supply Chain Management.

## <a name="functions"></a>Funkce
### <a name="purchase"></a>Nákup

Na kartě **Využití za měsíc (export)** vyberte **Nákup**, chcete-li ručně zaregistrovat množství získaných příspěvků.

Pro dané datum vyberte **Nový** a zadejte počet **Balíčků** získaných k tomuto datu.

**Množství** se počítá jako:

Množství = balíčky * 1 000

Vypočítané **Množství** odráží v **Zakoupeno** z indikátoru **Využití za měsíc (export)**.

### <a name="update"></a>Aktualizace

V podokně akcí vyberte **Aktualizovat** k aktualizaci výpočtu a aktualizaci údajů zobrazených na stránce a v grafu.

### <a name="reset-history-data"></a>Obnovit data historie

V podokně akcí vyberte **Obnovit data historie**, chcete-li aktualizovat databázi, ze které se počítají ukazatele.




> [!NOTE]
> Řídicí panel **Správa využití** nezobrazuje peněžní částky. Místo toho zobrazuje pouze objem počítaných odeslání a importovaných dokumentů.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
