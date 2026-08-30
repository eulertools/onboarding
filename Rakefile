require 'asciidoctor'
require 'rake/clean'
require 'rake/testtask'

OUTDIR = "public"
SOURCE = "README.adoc"
CLEAN.include(OUTDIR)


desc 'Render the docs'
task :html do
  sh "asciidoctor -d book -o #{OUTDIR}/index.html -n #{SOURCE}"
end

task :pdf do
  sh "asciidoctor-pdf -r asciidoctor-pdf README.adoc -o #{OUTDIR}/onboarding.pdf"
end

task :default => [:pdf, :html]
