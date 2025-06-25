# AD-Roofing-
import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Phone, Mail, MapPin } from "lucide-react";

export default function Home() {
  return (
    <main className="min-h-screen bg-gradient-to-br from-slate-100 to-white text-gray-800">
      <header className="bg-blue-900 text-white py-6 shadow-md">
        <div className="container mx-auto px-4 flex justify-between items-center">
          <h1 className="text-3xl font-bold">AD Roofing</h1>
          <nav className="space-x-4">
            <a href="#services" className="hover:underline">Services</a>
            <a href="#about" className="hover:underline">About</a>
            <a href="#contact" className="hover:underline">Contact</a>
          </nav>
        </div>
      </header>

      <section className="text-center py-16 px-4">
        <h2 className="text-4xl font-bold mb-4">Quality Roofing You Can Trust</h2>
        <p className="text-lg max-w-xl mx-auto mb-6">
          Protect your home with expert craftsmanship and reliable service from AD Roofing.
        </p>
        <Button size="lg">Get a Free Estimate</Button>
      </section>

      <section id="services" className="py-12 bg-slate-50">
        <div className="container mx-auto px-4 grid md:grid-cols-3 gap-6">
          {[
            { title: "Roof Repair", desc: "Fast and reliable roof repairs for leaks, damage, and wear." },
            { title: "New Roof Installation", desc: "High-quality roof installations for residential and commercial properties." },
            { title: "Roof Inspections", desc: "Thorough inspections to assess roof condition and maintenance needs." }
          ].map((service, index) => (
            <Card key={index} className="shadow-md">
              <CardContent className="p-6">
                <h3 className="text-xl font-semibold mb-2">{service.title}</h3>
                <p>{service.desc}</p>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      <section id="about" className="py-16 text-center px-4">
        <div className="max-w-2xl mx-auto">
          <h2 className="text-3xl font-bold mb-4">About AD Roofing</h2>
          <p>
            With over 20 years of experience, AD Roofing is committed to providing top-notch roofing solutions using the best materials and the latest techniques. Our licensed professionals ensure every job is done right the first time.
          </p>
        </div>
      </section>

      <section id="contact" className="py-16 bg-slate-100 px-4">
        <div className="max-w-xl mx-auto text-center">
          <h2 className="text-3xl font-bold mb-6">Get in Touch</h2>
          <div className="space-y-4">
            <p className="flex items-center justify-center gap-2"><Phone /> (123) 456-7890</p>
            <p className="flex items-center justify-center gap-2"><Mail /> contact@adroofing.com</p>
            <p className="flex items-center justify-center gap-2"><MapPin /> 123 Main Street, YourTown, USA</p>
          </div>
        </div>
      </section>

      <footer className="bg-blue-900 text-white text-center py-4">
        <p>&copy; {new Date().getFullYear()} AD Roofing. All rights reserved.</p>
      </footer>
    </main>
  );
}
