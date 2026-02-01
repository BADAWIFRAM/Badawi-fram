export const metadata = {
  title: "Badawi Farm",
  description: "Supplier Telur Ayam Petelur Jepara",
};

export default function RootLayout({
  children,
}: {
  children: React.ReactNode;
}) {
  return (
    <html lang="id">
      <body style={{ margin: 0 }}>{children}</body>
    </html>
  );
}
'use client';

import BadawiFarmWebsite from "@/components/BadawiFarmWebsite";

export default function Page() {
  return <BadawiFarmWebsite />;
}
'use client';

import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { motion } from "framer-motion";
import {
  ShoppingCart,
  Phone,
  MessageCircle,
  ShieldCheck,
  Truck,
  Egg,
} from "lucide-react";

const WA_NUMBER = "6282132698172";

const WA_MESSAGE = encodeURIComponent(`Halo Badawi Farm 👋

Saya ingin order / tanya harga telur ayam.

Nama:
Jenis pembelian (Eceran / Grosir):
Jumlah:
Alamat kirim:`);

export default function BadawiFarmWebsite() {
  return (
    <div className="min-h-screen bg-gradient-to-b from-[#0f172a] to-[#020617] text-white">

      {/* FLOATING WHATSAPP */}
      <a
        href={`https://wa.me/${WA_NUMBER}?text=${WA_MESSAGE}`}
        target="_blank"
        className="hidden md:flex fixed bottom-6 right-6 z-50 items-center gap-2 bg-green-500 hover:bg-green-600 px-5 py-3 rounded-full shadow-2xl"
      >
        <MessageCircle /> WhatsApp
      </a>

      {/* HERO */}
      <section className="container mx-auto px-6 py-24 text-center">
        <motion.h1
          initial={{ opacity: 0, y: 24 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.8 }}
          className="text-5xl md:text-6xl font-bold"
        >
          BADAWI FARM
        </motion.h1>

        <p className="mt-6 text-lg text-slate-300">
          Supplier Telur Ayam Berkualitas • Grosir & Eceran
        </p>

        <p className="mt-4 text-sm text-slate-400">
          📍 Slagi, Jepara – Jawa Tengah <br />
          Jl. Rangga Kusuma RT 13 / RW 03 <br />
          🕒 10.00 – 17.00 WIB
        </p>

        <div className="mt-10 flex justify-center gap-4 flex-wrap">
          <Button
            className="rounded-2xl px-8 py-6"
            onClick={() =>
              window.open(`https://wa.me/${WA_NUMBER}?text=${WA_MESSAGE}`, "_blank")
            }
          >
            <ShoppingCart className="mr-2" /> Pesan Sekarang
          </Button>

          <Button
            variant="outline"
            className="rounded-2xl px-8 py-6"
            onClick={() =>
              window.open(
                `https://wa.me/${WA_NUMBER}?text=Halo%20Badawi%20Farm,%20saya%20ingin%20bertanya`,
                "_blank"
              )
            }
          >
            <Phone className="mr-2" /> Hubungi Kami
          </Button>
        </div>
      </section>

      {/* INFO STOK */}
      <section className="text-center py-10">
        <div className="inline-block bg-emerald-500/10 border border-emerald-500/30 px-6 py-4 rounded-2xl">
          <p className="text-emerald-400 font-semibold text-lg">
            📦 Stok Hari Ini: TERSEDIA
          </p>
          <p className="text-sm text-slate-400">Update: Hari ini</p>
        </div>
      </section>

      {/* KEUNGGULAN */}
      <section className="container mx-auto px-6 py-16">
        <div className="grid md:grid-cols-3 gap-8">
          {[ 
            { icon: Egg, title: "Telur Segar", desc: "Langsung dari peternak" },
            { icon: ShieldCheck, title: "Kualitas Terjaga", desc: "Sortir & bersih" },
            { icon: Truck, title: "Pengiriman", desc: "Area sekitar Jepara" }
          ].map((item, i) => (
            <Card key={i} className="bg-white/5 border-white/10 rounded-2xl">
              <CardContent className="p-8 text-center">
                <item.icon className="mx-auto mb-4 text-amber-400" size={36} />
                <h3 className="text-xl font-semibold">{item.title}</h3>
                <p className="text-slate-300 text-sm">{item.desc}</p>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      {/* FOOTER */}
      <footer className="text-center py-12 text-slate-400">
        <p className="text-white font-semibold">BADAWI FARM</p>
        <p>Peternakan & Supplier Telur Ayam</p>
        <p className="text-sm mt-2">
          © {new Date().getFullYear()} Badawi Farm
        </p>
      </footer>

      {/* MOBILE CTA */}
      <div className="fixed bottom-0 left-0 right-0 md:hidden bg-[#020617] p-4">
        <Button
          className="w-full py-6 rounded-xl"
          onClick={() =>
            window.open(`https://wa.me/${WA_NUMBER}?text=${WA_MESSAGE}`, "_blank")
          }
        >
          <ShoppingCart className="mr-2" /> Order via WhatsApp
        </Button>
      </div>

    </div>
  );
}
