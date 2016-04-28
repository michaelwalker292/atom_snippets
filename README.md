# Your snippets
'.source.js':
  '.mocha initial':
    'prefix': 'minit'
    'body': """'use strict'

      var chai = require('chai')
      var expect = chai.expect

      describe('Given $1', function() {
        describe('When ', function() {
          it('Then ', function() {

          })
        })
      })
        """
  '.describe, describe and it':
    'prefix': 'ddi'
    'body': """describe('Given $1', function() {
        describe('When ', function() {
          it('Then ', function() {

          })
        })
      })
      """

  '.describe and it':
    'prefix': 'di'
    'body': """describe('When $1', function() {
        it('Then ', function() {

        })
      })
      """
  '.mocha it':
    'prefix': 'it'
    'body': """it('Then $1', function() {

        })
      """

  '.supertest setup':
    'prefix': 'sts'
    'body': """'use strict'

      var request = require('supertest')
      var app = require('../../app')

      describe('Given $1', function() {
        describe('When ', function() {
          it('Then ', function(done) {

          })
        })
      })
        """
  '.protractor setup':
    'prefix': 'ps'
    'body': """'use strict'

      var http = require('http')
      var expect = require('chai').expect

      var server

      before(function () {
        server = http.createServer(require('../../app'))
        server.listen(0)
        browser.baseUrl = 'http://localhost:' + server.address().port
      })

      beforeEach(function () {
        browser.ignoreSynchronization = true
      })

      after(function () {
        server.close()
      })

      describe('Given $1', function() {
        describe('When ', function() {
          it('Then ', function(done) {

          })
        })
      })
      """

  '.express router setup':
    'prefix': 'ers'
    'body': """'use strict'

      var express = require('express')
      var router = express.Router()

      router.get('/', function(req, res, next) {
        res.sendStatus(200)
      });

      module.exports = router
      """
